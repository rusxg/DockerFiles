FROM alpine:3.4

RUN \
	apk update && \
	apk add g++ gcc make bash ca-certificates openssl wget && \
	wget https://cmake.org/files/v3.7/cmake-3.7.1.tar.gz && \
	tar xvf cmake-3.7.1.tar.gz && \
	/bin/bash -c "cd cmake-3.7.1 && \
		./configure && \
		make && \
		make install && \
		cd .. && rm -rf cmake-3.7.1 && \
		rm cmake-3.7.1.tar.gz" && \
	rm -rf /var/cache/apk/*