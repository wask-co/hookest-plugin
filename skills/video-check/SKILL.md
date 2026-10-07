---
name: video-check
description: Score the opening of the user's own video with the Hookest Virality Predictor before they post it, and explain what holds it back. Use when the user asks to score, rate, review or check their video, Reel, TikTok or Short, asks if it will go viral, or asks how to improve their first 3 seconds.
---

# Video check with the Hookest Virality Predictor

Goal: get the user an official Hookest score (0 to 100) for the opening of a
video file on their machine, then turn the result into concrete fixes.

## What it can and cannot do

- It scores the OPENING of a video FILE against proven viral hooks. It does not
  estimate view counts. If asked for views, say so and offer the score.
- It needs a file, not a link. For an Instagram or TikTok link, ask the user to
  save the video and give you the file path.
- The first analysis is free, after that it needs Hookest Pro. Call
  `get_account` first if you are unsure. If a limit is hit, link the
  `upgrade_url` the tool returns and never quote a price that did not come from
  `get_account`.

## Steps

1. **Find the file.** Use the path the user gave. If they did not give one, ask
   for it in one question.

2. **Read duration and size.** Run
   `ffprobe -v error -show_entries format=duration,size -of default=nw=1 "<file>"`.
   If `ffprobe` is missing, use `stat` for the size and ask the user for the
   length, or skip to the fallback in step 6.

3. **Check the limits.** The upload takes mp4 only, up to 32 seconds and 40 MB.
   - Not mp4, or longer than 32 seconds: offer to make a copy of the first 30
     seconds with
     `ffmpeg -i "<file>" -t 30 -c:v libx264 -c:a aac "<file>-hookest.mp4"`.
     Only the opening is scored, so nothing is lost. Ask before running it and
     never overwrite the original.

4. **Upload.** Call `upload_prediction_video` with `duration_seconds`, `bytes`
   and the user's `language`. It reserves one analysis and returns a one-time
   upload URL and a ready `curl` command. Run that command with the real file
   path. Do not change the URL.

5. **Score.** Call `run_prediction` with the `prediction_id`. If the status is
   `queued` or `running`, wait a few seconds and call `get_prediction` with the
   same id until it finishes.

6. **Fallback.** If the upload fails or the file cannot be read, call
   `start_prediction` and give the user its `upload_url` to upload in the
   browser. Then call `get_prediction` when they say it is done.

## Output

- The score and its band, exactly as returned
- What holds the opening back, in the tool's own terms, then 2 or 3 concrete
  edits for the first seconds (cut, text on screen, first line, first visual)
- If it fits, 2 or 3 real library hooks from `find_hooks` in the same niche to
  borrow an opening from, with their Hookest links

If the user wants to compare with earlier videos, call `list_predictions` and
`get_prediction` with the ids they mean.
