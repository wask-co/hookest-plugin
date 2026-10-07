# Image sources

`banner.png` and `how-it-works.png` are rendered from the HTML files here.
After editing one, re-render it (2x for sharp text):

```
CHROME="/Applications/Google Chrome.app/Contents/MacOS/Google Chrome"
"$CHROME" --headless --disable-gpu --hide-scrollbars --force-device-scale-factor=2 \
  --virtual-time-budget=5000 --window-size=1280,640 \
  --screenshot=../banner.png "file://$PWD/banner.html"
"$CHROME" --headless --disable-gpu --hide-scrollbars --force-device-scale-factor=2 \
  --virtual-time-budget=5000 --window-size=1280,440 \
  --screenshot=../how-it-works.png "file://$PWD/how-it-works.html"
```

Run from this folder. Colors and font (Plus Jakarta Sans) follow hookest.com.
