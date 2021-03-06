# protobuf 3 docker

[on docker hub](https://registry.hub.docker.com/u/nanoservice/protobuf/)

Tiny docker image with protoc 3.

Part of nanoservice docker image library.

## Usage

    # Just print protobuf help message
    docker run -it --rm \
      nanoservice/protobuf --help

    # Use current folder for input and output
    docker run -it --rm -v $PWD:/src:rw \
      nanoservice/protobuf --cpp_out=. *.proto

    # If you ran into problems with user uid and gid (consider scripting it)
    docker run -it --rm -v $PWD:/user-src:rw -u $(id -u):$(id -g) -w /user-src \
      nanoservice/protobuf --cpp_out=. *.proto

## Contributing

1. Fork it ( https://github.com/nanoservice/docker-protobuf/fork )
1. Create your feature branch (git checkout -b my-new-feature)
1. Commit your changes (git commit -am 'Add some feature')
1. Push to the branch (git push origin my-new-feature)
1. Create a new Pull Request

## Contributors

* [waterlink](https://github.com/waterlink) Oleksii Fedorov, creator, maintainer
