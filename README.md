# hohwebm (work in progress)
AV1 webms with less headache

A bash script for encoding AV1 clips

# Requirements
- ffmpeg (sudo apt install ffmpeg)
- aomenc (see 'installing aomenc')

# Install

Place in PATH, for instance in:
```
sudo cp hohwebm.sh /usr/local/bin/hohwebm.sh
```

# Usage

```
hohwebm.sh video [start [end [profile [...aom options]]]]
```
example:  
```
hohwebm.sh anime\ ep1.mkv 10:23 10:30.2 anilist
```
(this is currently also the only implemented syntax)

parameters:  
```
  start          :  timestamp (hint: mpv gives you decimal seconds if you click on the time)
  end            :  timestamp
  profile        :  predefined set of encoding parameters. Included: 'anilist', 'anilist-slow', 'anilist-fast' and 'default'
  ...aom options :  every other option is passed to aomenc as a parameter. Overrides profile defaults.
```

# Limitations

- No sound (TODO)
- No subtitles (TODO)
