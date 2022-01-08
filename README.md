Requirements:
```
brew install protobuf
conda create -n protobuf python=3.8
conda activate protobuf
pip install -r requirements.txt
```

Compiling your protocol buffers for python:
```
#protoc -I=$SRC_DIR --python_out=$DST_DIR $SRC_DIR/addressbook.proto
protoc -I=./protobuf --python_out=./src/python ./protobuf/addressbook.proto
```

Running example:
```
python src/python/write.py addressbook.data
file addressbook.data
cat addressbook.data
python src/python/read.py addressbook.data
```
