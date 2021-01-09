FROM ubuntu

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y wget cmake g++ clang libboost-all-dev libbenchmark-dev && apt-get clean && rm -rf /var/lib/apt/lists/* 
RUN wget https://github.com/google/googletest/archive/release-1.10.0.tar.gz && tar -xvzf release-1.10.0.tar.gz && cd googletest-release-1.10.0 && cmake -DBUILD_SHARED_LIBS=ON . && make && cp -a googletest/include/gtest /usr/include && cp lib/libg* /usr/lib/
