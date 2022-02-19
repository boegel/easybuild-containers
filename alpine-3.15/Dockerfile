FROM alpine:3.15
RUN apk add --no-cache curl lua-filesystem lua-posix python3 tcl-dev \
&& apk add --no-cache gcc g++ \
&& curl -OL https://github.com/TACC/Lmod/archive/refs/tags/8.6.12.tar.gz && tar xfz 8.6.12.tar.gz && rm 8.6.12.tar.gz \
&& cd Lmod-8.6.12 && ./configure && make install && cd - \
&& apk del curl
