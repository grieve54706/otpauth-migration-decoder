# otpauth migration decoder

Convert Google Authenticator data to plain otpauth links


## usage

1. get QR code in "Google Authenticator" app (Menu → Transfer accounts → Export accounts → Select accounts → Next)
1. extract link from QR code with your preferred [QR codes reading software](https://play.google.com/store/search?q=qr%20code%20reader)
1. pass migration link (`otpauth-migration://offline?data=...`) to this tool

## requirements

The protobuf package is required to running this script:

```.shell
$ pip install protobuf
$ pip install click
```

## example

```
$ python decoder.py --convert "otpauth-migration://offline?data=CjEKCkhlbGxvId6tvu8SGEV4YW1wbGU6YWxpY2VAZ29vZ2xlLmNvbRoHRXhhbXBsZTAC"
```


## references

1. [otpauth:// URI format](https://github.com/google/google-authenticator/wiki/Key-Uri-Format)
1. [Protocol Buffer Basics: Python](https://developers.google.com/protocol-buffers/docs/pythontutorial)
1. [Authenticator live demo](https://rootprojects.org/authenticator/)
