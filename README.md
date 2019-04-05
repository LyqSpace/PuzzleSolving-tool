# PuzzleSolving-tool

This is a package contains three tools for puzzle solving:

1. Generator in Python.
2. Generator in Javascript (deprecated). [link](https://lyqspace.github.io/PuzzleSolving-tool/generator.html)
3. Debugger in Javascript. [link](https://lyqspace.github.io/PuzzleSolving-tool/debugger.html)

## Usages

### Generator in Python

A tool for generating puzzles.

optional arguments:

| option | value | description |
| ---- | ---- | ---- |
| -h --help | | show this help message and exit |
| -i | IMG_PATH | Path to the input image. |
| -n | PIECE_N | Number of puzzle pieces. Default is 10. The actual number of puzzle pieces may be different. |
| -t | SAMPLE_N | Number of puzzle you want to generate from the input image. Default is 1. |
| --offset-h | OFFSET_H | Provide the horizontal offset rate when chopping the image. Default is 1. The offset is the rate of the initial rigid piece height. If the value is less than 0.5, no interaction will happen. |
| --offset-w | OFFSET_W | Provide the vertical offset rate when chopping the image. Default is 1. The offset is the rate of the initial piece width. If the value is less than 0.5, no interaction will happen. |
| -s | SMALL_REGION | A threshold controls the minimum area of a region with respect to initial rigid piece area. Default is 0.25. |
| -r | ROTATE | A range of random rotation (in degree) applied on puzzle pieces. Default is 180. The value should be in \[0, 180\]. Each piece randomly select a rotation degree in \[-r, r\] |
| --blank_color | BLANK_COLOR | Blank color to fill the empty area. Default is \[0, 0, 0\]. The type is three uint8 numbers in BGR OpenCV format. |

The output file tree is:
.
├── data
│   ├── puzzles
│   │   ├── 0
│   │   │   ├── config.txt
│   │   │   ├── groundtruth.json
│   │   │   ├── groundtruth.txt
│   │   │   ├── puzzle-0.zip
│   │   │   ├── piece-0.png
│   │   │   ├── piece-1.png
│   │   │   ├── piece-2.png
│   │   │   ├── piece-3.png
│   │   │   └── ....
│   │   ├── 1
│   │   │   ├── config.txt
│   │   │   ├── groundtruth.json
│   │   │   ├── groundtruth.txt
│   │   │   ├── puzzle-1.zip
│   │   │   ├── piece-0.png
│   │   │   ├── piece-1.png
│   │   │   ├── piece-2.png
│   │   │   ├── piece-3.png
│   │   │   └── ....
│   │   └── ....

### Debugger in Javascript

1. Upload a package of pieces, which must contains: 
