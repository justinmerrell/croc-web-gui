# croc Preperation

**As of croc release v9.6.0 the official repo requires the use if go module package machineid, incompatible with js requirements. A fork of croc with this requirement can be found [here](https://github.com/justinmerrell/croc).**

An additional change is the use of os.UserHomeDir() which is not supported in js.
Only single files can be downloaded, to receive a directory the user must zip it first.
croc will write the file to a blob first then prompt the user to download it.


Clone croc repo and chang directory to croc.

Relies on a 3rd party to retrive the ip address, could be replaced internally.

```bash
cp "$(go env GOROOT)/misc/wasm/wasm_exec.js" .
GOOS=js GOARCH=wasm go build -o main.wasm
'''
