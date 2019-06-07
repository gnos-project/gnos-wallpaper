<div align="center"><p align="center"><img src="https://gnos.in/img/shot/common/gnos-wallpaper-selector_1.png"></img></p></div>

# GNOS Wallpaper

GUI & CLI to setup GNOME wallpaper from subreddits

## Usage

```
USAGE: wallpaper-selector [OPTS] ...
  -p  Number of pages to query (100 images)
  -r  Subreddit, e.g. 'museum+ArtPorn'
  -f  Filter by title regex, e.g. '[^0-9a-z\\[]+1[4-7][0-9][0-9][^0-9a-z\\]]'
  -s  Sort, e.g. 'hot', 'new', 'controversial', 'top', 'rising'
  -h  This help screen
```

Examples:

```bash
# Get 100 images from r/wallpaper
wallpaper-selector -r wallpaper

# Get 4 pages from r/museum+ArtPorn then filter titles for 1400-1799.
wallpaper-selector -p 4 -r museum+ArtPorn -f '[^0-9a-z\\[]+1[4-7][0-9][0-9][^0-9a-z\\]]'
```

## Automation

Alternatively you can automate using the CLI adapted from [reddit-wallpaper](https://github.com/NuLL3rr0r/reddit-wallpaper):

```bash
# Use a random pic from r/wallpaper, fullscreen fit
wallpaper -z -r r/wallpaper -o zoom

# Use a random pic from r/museum+ArtPorn, filter titles, fit, black bg
wallpaper -z -r r/museum+ArtPorn -f '[^0-9a-z\\[]+1[4-7][0-9][0-9][^0-9a-z\\]]' -o scaled -b 000000
```

## Install

Just copy scripts somewhere in your `$PATH`.

Depends on [YAD](https://sourceforge.net/projects/yad-dialog/) `jq` `wget` `pkill` `gsettings`.

## Credits

Original idea by [Mamadou Babaei](https://github.com/NuLL3rr0r/reddit-wallpaper).
