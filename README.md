change head or swap face

use seetaface & dlib

1. git clone dlib from https://github.com/davisking/dlib
2. git clone seetaface from https://github.com/seetaface/SeetaFaceEngine
3. install opencv or from source https://github.com/opencv/opencv
4. build all of up
5. make sure dlib & seetaface in same parent folder as this project for config
6. linux system , use ``CMakeLists.txt.linux``
7. build

```
cd facedlib
mkdir release
cmake ..
make install -j4
```

8. get ``libfaceB.so``
9. use it.


# how to use

```
int init(const char * dir, const char* model2)

dir - directory of pictures
model2 - file of landmarks, you can download it from http://dlib.net/files/shape_predictor_68_face_landmarks.dat.bz2

set_outpath(const char *a)
a - filename , for example 1.jpg
```

u must run init&set_outpath at first and once

```
return -1 if failed, otherwise success
a - photo of head given
b - model of body
int swap_head(const char *a, const char *b)

return -1 if failed, otherwise success
a - photo of face given
b - model of body
int swap_face(const char *a, const char *b)
```
