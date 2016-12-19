FROM rusxg/alpine-cmake-ffmpeg

ENV CC /usr/bin/clang
ENV CXX /usr/bin/clang++
RUN \
	apk update  && \
	apk add unzip ca-certificates jpeg-dev openssl \
            libpng-dev tiff-dev linux-headers clang  && \
	wget https://codeload.github.com/opencv/opencv/zip/3.1.0 && \
	unzip 3.1.0 && \
	/bin/bash -c "cd opencv-3.1.0 && \
		mkdir build && cd build && \
                cmake -D CMAKE_BUILD_TYPE=RELEASE \
                      -D WITH_IPP=OFF .. && \
                make && \
		make install && \
		cd .. && rm -rf opencv-3.1.0 \
		" && \
	rm -rf /var/cache/apk/*