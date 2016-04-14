FROM ubuntu:14.04

RUN set -xe \
	\
	&& sudo apt-get install software-properties-common -y \
	\
	&& sudo add-apt-repository ppa:ubuntu-toolchain-r/test \
	&& sudo apt-get update -y \
	&& sudo apt-get upgrade -y \
	\
	&& sudo apt-get install gcc-4.8 g++-4.8 \
	&& sudo apt-get install gcc-4.9 g++-4.9 \
	&& sudo apt-get install gcc-5 g++-5 \
	\
	&& sudo updatedb && sudo ldconfig

RUN sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.8 48 \
	--slave /usr/bin/gcc-ar gcc-ar /usr/bin/gcc-ar-4.8 \
	--slave /usr/bin/gcc-nm gcc-nm /usr/bin/gcc-nm-4.8 \
	--slave /usr/bin/gcc-ranlib gcc-ranlib /usr/bin/gcc-ranlib-4.8

RUN sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-4.8 48 \
	--slave /usr/bin/g++-ar g++-ar /usr/bin/g++-ar-4.8 \
	--slave /usr/bin/g++-nm g++-nm /usr/bin/g++-nm-4.8 \
	--slave /usr/bin/g++-ranlib g++-ranlib /usr/bin/g++-ranlib-4.8

RUN sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-4.9 49 \
	--slave /usr/bin/gcc-ar gcc-ar /usr/bin/gcc-ar-4.9 \
	--slave /usr/bin/gcc-nm gcc-nm /usr/bin/gcc-nm-4.9 \
	--slave /usr/bin/gcc-ranlib gcc-ranlib /usr/bin/gcc-ranlib-4.9

RUN sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-4.9 49 \
	--slave /usr/bin/g++-ar g++-ar /usr/bin/g++-ar-4.9 \
	--slave /usr/bin/g++-nm g++-nm /usr/bin/g++-nm-4.9 \
	--slave /usr/bin/g++-ranlib g++-ranlib /usr/bin/g++-ranlib-4.9

RUN sudo update-alternatives --install /usr/bin/gcc gcc /usr/bin/gcc-5 53 \
	--slave /usr/bin/gcc-ar gcc-ar /usr/bin/gcc-ar-5 \
	--slave /usr/bin/gcc-nm gcc-nm /usr/bin/gcc-nm-5 \
	--slave /usr/bin/gcc-ranlib gcc-ranlib /usr/bin/gcc-ranlib-5

RUN sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-5 53 \
	--slave /usr/bin/g++-ar g++-ar /usr/bin/g++-ar-5 \
	--slave /usr/bin/g++-nm g++-nm /usr/bin/g++-nm-5 \
	--slave /usr/bin/g++-ranlib g++-ranlib /usr/bin/g++-ranlib-5

# overwrite this with 'CMD []' in a dependent Dockerfile
CMD ["/bin/bash"]
