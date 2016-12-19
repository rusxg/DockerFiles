FROM rusxg/alpine-cmake

RUN \
	apk update && \
	apk add coreutils yasm && \
	wget http://ffmpeg.org/releases/ffmpeg-3.2.2.tar.bz2 && \
	tar xvf ffmpeg-3.2.2.tar.bz2 && \
	/bin/bash -c "cd ffmpeg-3.2.2 && \
		./configure && \
		make && \
		make install && \
		cd .. && rm -rf ffmpeg-3.2.2 \
		" && \
	rm -rf /var/cache/apk/*