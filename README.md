# NETPIGIX

## Motivation
* Issues of the default NETFLIX video player
  - cannot turn subtitle on/off via shortcut keys
  - right after a character says a line, the subtitle disappears
* This extension is meant to solve the above issues

## Installation
Since this extension is not published to the official Chrome Web Store, you have to do the following;
* git clone or download this
* open your Chrome and go to Extensions settings `chrome://extensions/`
* turn `Developer mode` on
* `Load unpacked` and select this directory

## Usage
* You may have to reload the page `https://www.netflix.com/watch/*` to activate the extension.
* Press `Alt` or `option` key to toggle the custom subtitle.

## DOM structure of the Netflix watch-video page (extracted only the relevant part)
memo for development purpose

```
.VideoContainer
  - #netpigix-subtitle-contaner (This will be added by this extension)
    - .netpigix-text
    - .netpigix-text
    - ...
  - div
    - video
    - .player-timedtext (dinamically generated)
      - .player-timedtext-text-container
        - span
        - span
        - ...
```
