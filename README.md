# ffmpeg_commend
자주쓰는 ffmpeg commend


```
ffmpeg -i input-file.mp4 -c:v libvpx -crf 10 -b:v 1M -c:a libvorbis output-file.webm
```

→ 압축율 좋으나 홍조현상



```
ffmpeg -i input.mp4 -c:v libvpx-vp9 -b:v 1M -c:a libvorbis output.webm
```

→ webm 원본에 가깝게 압축


```
ffmpeg -i 01_kpop_cover_kor.mp4 -vcodec h264 -movflags +faststart -an 01_kpop_cover_kor2.mp4

ffmpeg -i a.mp4 -vf scale=1280x720 -vcodec h264 -movflags +faststart -an bb.mp4
```

```
폴더 전체
for file in *.mp4

do

ffmpeg -i "$file" -vcodec h264 -movflags +faststart "./dist/${file%.*}.mp4"

done
```


```

→ mp4 압축


```
ffmpeg -i RPReplay_Final1701842315.mp4 -vp9 h264 -movflags +faststart -an busan2.webm
```

```
ffmpeg -i busan.mp4 -c:v libvpx-vp9 -movflags +faststart -b:v 1M -c:a libvorbis output2.webm
```
->  webm 변환
