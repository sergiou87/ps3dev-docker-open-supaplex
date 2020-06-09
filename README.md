# ps3dev-docker-open-supaplex

## What does this do?
This program will automatically build a docker image with the ps3dev toolchain ready to be used for PS3 homebrew development.

In particular, this image uses the official toolchain (using flipacholas/ps3devextra image as base) and installs SDL2, SDL2_mixer, debugnet and the latest versions of libogg and libvorbis on top of that.

This image is specifically made to build [OpenSupaplex](https://github.com/sergiou87/open-supaplex/) for PS3.

## How do I build it?

#### Build the image:
`sudo docker build -t ps3dev-docker .`

#### Copy the helper script:
`sudo cp ps3dev-docker /usr/local/bin`

## How do I use it?

#### Use the helper script to run commands in the current directory:
`ps3dev-docker make`

## How do I save and load it?

#### Save the image:
`sudo docker save ps3dev-docker | bzip2 > ps3dev-docker.tar.bz2`

#### Load the image:
`sudo docker load < bzip2 -dc ps3dev-docker.tar.bz2`

## How do I remove it?

#### Remove the image:
`sudo docker rmi ps3dev-docker`

#### Remove the helper script:
`sudo rm /usr/local/bin/ps3dev-docker`
