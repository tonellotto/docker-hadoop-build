docker-hadoop-build
===================

## Build Apache Hadoop

Often when we use Apache Hadoop and would like to make a custom build (stock or forked) you'll have to rebuild the whole Hadoop, native libs, etc ... which takes 30+ minutes, and carries lots of dependencies (libraries, protobuf, etc - at a given version).

This Docker image contains the build process of Hadoop 2.9.1 nativelibs.

## Build the image

```
docker build -t pad/hadoop-nativelibs .
```

## Copy the tarred libs from docker container

```
docker run --rm  sequenceiq/hadoop-nativelibs > hadoop-native-64-2.9.1.tar
```
