# FFMPEG commands

# Embed subtitles
```bash
ffmpeg -i input.mp4 -i subtitles.srt -c:v copy -c:a copy -c:s mov_text output.mp4
```

# Merge multiple videos
```bash
ffmpeg -i "input1.mp4[input1] -i "input2.mp4[input2] -i "input3.mp4[input3] -filter_complex "[input1][input2][input3]concat" -c:v libx264 -c:a aac -movflags faststart output.mp4
```
