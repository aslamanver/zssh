# ZSSH - ZIP over SSH
#### Simple Python script to exchange files between servers.

Login to SSH and choose which path you need to serve over HTTP.

> This script is based on Python 3+

Intall 
```sh
python3 -m pip install zssh
```

Expose a directory to `ZIP`
```sh
$ zssh -as --path /desktop/path_to_expose
```

Extract a `ZIP` from URL
```sh
$ zssh -ad --path /desktop/path_to_download --zip http://mydomain.com/temp_file.zip
```

Execute the script using remote URL
```sh
python3 <(wget -o /dev/null https://aslamanver.github.io/zssh/zssh/zssh.py -q -O-) -h
```

Usage
```bash
usage: zssh [-h] -a A --path PATH [--zip ZIP] [--port PORT]

required arguments:
  -a A         Action [s = serve, d = download]
  --path PATH  File/Folder Path

optional arguments:
  --zip ZIP    ZIP File URL | Name should be *.zip
  --port PORT  Server Port | Default: 9800
```
