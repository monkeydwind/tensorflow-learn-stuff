# tensorflow-learn-stuff
All TF learning stuff

## Docker
	- Dockerfile-opencv - Docker file to build image with python 3.7 + opencv 3.4.10
	  build image: docker build -t base-opencv -f Dockerfile-opencv .
	- Dockerfile-tensorflow - Docker file to build image with python 3.7 + tensorflow 2.1 source code, for build wheel
	  build image: docker build -t source-tensorflow -f Dockerfile-tensorflow .
	- Dockerfile-opencv-tensorflow - Docker file to build image with python 3.7 + opencv 3.4.10 + tensorflow 2.1
	  build image: docker build -t base-tensorflow -f Dockerfile-opencv-tensorflow . 
	
## Wheels
    - tensorflow-2.1.0-cp37-cp37m-linux_x86_64-cpu.whl - Intel optimize with all feature enable, build on top of python 3.7
    - tensorflow-2.1.0-cp36-cp36m-linux_x86_64.whl - Intel optimize with all feature enable, build on top of python 3.6
    build with options:
    bazel build -c opt --copt=-mavx --copt=-mavx2 --copt=-mfma --copt=-msse4.2 //tensorflow/tools/pip_package:build_pip_package