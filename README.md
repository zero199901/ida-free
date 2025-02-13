


magnet:?xt=urn:btih:E494D762231641470B885398F577BC2624DC8AE1&tr=http%3A%2F%2Fbt4.t-ru.org%2Fann%3Fmagnet&dn=IDA%20Pro%209.0.241217%20SP1%20(Win%2FMac%2FLinux)%20%2B%20SDK%20and%20utilities%20%5B2024%2C%20ENG%5D

磁力地址

之前如果装过beta，先卸载。
安装RC1。
把kg_patch里的keygen2.py copy到/Applications/IDA\ Professional\ 9.0.app/Contents/MacOS
依次执行以下操作（其实就是keygen，然后替换libida*.dylib 以及codesign）
 复制代码 隐藏代码
python keygen2.py
cp libida.dylib.patched libida.dylib
cp libida32.dylib.patched libida32.dylib
cp 
sudo xattr -cr /Applications/IDA\ Professional\ 9.0.app
sudo codesign -f -s - /Applications/IDA\ Professional\ 9.0.app/Contents/MacOS/libida.dylib
sudo codesign -f -s - /Applications/IDA\ Professional\ 9.0.app/Contents/MacOS/libida32.dylib
最后 将keygen生成的许可证idapro.hexlic放在~/.idapro/
