# Protobuf Files


## Protoc

https://github.com/protocolbuffers/protobuf/releases/tag/v22.3

## Python Code Generate

```shell
pip install grpcio-tools
mkdir ../py_gen
python -m grpc_tools.protoc -I ./ --python_out=../py_gen --pyi_out=../py_gen --grpc_python_out=../py_gen .\pb.proto  
```

[python Grpc](https://grpc.io/docs/languages/python/)

## Dart Code Generate

```shell
dart pub global activate protoc_plugin
mkdir ../lib/src/dart_gen
protoc -I ./ ./pb.proto --dart_out=grpc:../lib/src/dart_gen
```

[dart grpc](https://grpc.io/docs/languages/dart/)


## Add Proto file as Submodule

- add

```shell
git submodule add -- git@github.com:better-todolist/proto_files.git .\Protos\pb
```

- update ``git submodule foreach git pull``
