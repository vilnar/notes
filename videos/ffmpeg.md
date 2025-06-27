## convert mov to gif

create folder `frames`

```
ffmpeg -i input.mov -r 15 frames/image-%3d.png
ffmpeg -i input.mov -r 15 -vf scale=680:-1 frames/image-%3d.jpg
```

### Generate the sprite sheet

```
ffmpeg -y -i input.mov -frames 1  -q:v 2 -filter_complex "fps=10,pad=width=max(iw\,ih*(16/9)):height=ow/(16/9):x=(ow-iw)/2:y=(oh-ih)/2,scale=-1:383:force_original_aspect_ratio=decrease,tile=1x32" frames/image-%3d.jpg
ffmpeg -y -i input.mov -frames 1  -q:v 2 -filter_complex "fps=10,pad=width=max(iw\,ih*(16/9)):height=ow/(16/9):x=(ow-iw)/2:y=(oh-ih)/2,scale=-1:259:force_original_aspect_ratio=decrease,tile=1x32" frames/image-mobile-%3d.jpg
```


```
ffmpeg -i input.mov -vf "fps=15,scale=680:-1:flags=lanczos,split[s0][s1];[s0]palettegen[p];[s1][p]paletteuse" -loop -1 loader-desktop.gif
ffmpeg -i input.mov -vf "fps=15,scale=460:-1:flags=lanczos,split[s0][s1];[s0]palettegen[p];[s1][p]paletteuse" -loop -1 loader-mobile.gif
ffmpeg -i input.mov -vf "fps=10,scale=460:-1:flags=lanczos,split[s0][s1];[s0]palettegen[p];[s1][p]paletteuse" -loop -1 loader-mobile.gif
ffmpeg -i input.mov -vf "fps=25,scale=680:-1:flags=lanczos,split[s0][s1];[s0]palettegen[p];[s1][p]paletteuse" -loop -1 loader-desktop1.gif
ffmpeg -i input.mov -vf "fps=25,scale=460:-1:flags=lanczos,split[s0][s1];[s0]palettegen[p];[s1][p]paletteuse" -loop -1 loader-mobile1.gif
```


GIF
```
ffmpeg -framerate 15 -i frames/image-%3d.png -loop -1 output.gif
ffmpeg -framerate 30 -i frames/image-%3d.jpg -loop -1 output.gif
ffmpeg -framerate 15 -start_number 022 -i frames3/image-%3d.png -loop -1 output.gif

ffmpeg -framerate 15 -i png/image-%3d.png -loop -1 -filter_complex paletteuse -r 10  output.gif
ffmpeg -framerate 15 -i png/image-%3d.png -loop -1 -s 660x290 output.gif
ffmpeg -framerate 15 -i png/image-%3d.png -loop -1 -s 660x290 output.gif
```

