# open_cobot
Open and license-free robot arm project with 3D printer. I will add 3D CAD models, my diary about how to develop robots, and ROS packages for them


## Preparation
### Docker

~~~
cd open_cobot
docker build -f docker/dockerfile -t humble . 
docker run --rm -it --privileged --net=host --ipc=host \
    -v $PWD:/home/ubuntu/open_cobot/ \
    -v /tmp/.X11-unix:/tmp/.X11-unix \
    -e DISPLAY=$DISPLAY \
    -v $HOME/.Xauthority:/home/$(id -un)/.Xauthority \
    -e XAUTHORITY=/home/$(id -un)/.Xauthority \
    humble bash
~~~