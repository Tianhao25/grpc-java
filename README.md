# grpc-java

## grpc
gRPC is really attractive to me when it was first introduced to me by Bittiger teacher. Now, I would like to try it out. 

## Basics
**Protocal Buffers**: https://developers.google.com/protocol-buffers/ Is a google based, lauguage neutral, service define protocal.  
**Install Protocal Buffer on MacOS**: 
```bash
$ brew install protobuf  
```
> **Install Protocal Buffer gRPC-Java Plugin**:   
> 1. git clone https://github.com/grpc/grpc-java.git
> 2. Go to ./compliler folder  
> 3. run **$ ../gradlew java_pluginExecutable**
> 4. run **$ ../gradlew test** to verify result
> 5. Try with following command to compile your first proto:
> ```bash
> $ protoc --plugin=protoc-gen-grpc-java=build/exe/java_plugin/protoc-gen-grpc-java \
>  --grpc-java_out="$OUTPUT_FILE" --proto_path="$DIR_OF_PROTO_FILE" "$PROTO_FILE"
> ```
> Build gRPC independent java code:
> ```bash
> protoc -I=$SRC_DIR --java_out=$DST_DIR $SRC_DIR/addressbook.proto
> ```
> 6. You will find a xxxGrpc file and other helper files generated there!


## Kengs
parseUnknownFieldProto3 can not found: Try to import this:
```
<!-- https://mvnrepository.com/artifact/com.google.protobuf/protobuf-java -->
<dependency>
    <groupId>com.google.protobuf</groupId>
    <artifactId>protobuf-java</artifactId>
    <version>3.4.0</version>
</dependency>
```
