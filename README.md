


magnet:?xt=urn:btih:E494D762231641470B885398F577BC2624DC8AE1&tr=http%3A%2F%2Fbt4.t-ru.org%2Fann%3Fmagnet&dn=IDA%20Pro%209.0.241217%20SP1%20(Win%2FMac%2FLinux)%20%2B%20SDK%20and%20utilities%20%5B2024%2C%20ENG%5D

磁力地址


# IDA Pro 9.0 RC1 安装与激活操作步骤

---

## 1. 卸载旧版（如有安装过 beta 版）

如果之前安装过 beta 版，建议先卸载：

```bash
sudo rm -rf /Applications/IDA\ Professional\ 9.0.app
```

---

## 2. 安装 RC1 版本

- 安装 IDA Pro 9.0 RC1 到 `/Applications/IDA Professional 9.0.app`

---

## 3. 拷贝 keygen2.py 到指定目录

将 `kg_patch` 文件夹中的 `keygen2.py` 拷贝到：

```
/Applications/IDA Professional 9.0.app/Contents/MacOS/
```

---

## 4. 依次执行以下命令

进入该目录：

```bash
cd /Applications/IDA\ Professional\ 9.0.app/Contents/MacOS/
```

### 4.1 运行 keygen 生成补丁和许可证

```bash
python keygen2.py
```

### 4.2 替换动态库文件

```bash
cp libida.dylib.patched libida.dylib
cp libida32.dylib.patched libida32.dylib
```

### 4.3 清除应用属性

```bash
sudo xattr -cr /Applications/IDA\ Professional\ 9.0.app
```

### 4.4 重新签名动态库

```bash
sudo codesign -f -s - /Applications/IDA\ Professional\ 9.0.app/Contents/MacOS/libida.dylib
sudo codesign -f -s - /Applications/IDA\ Professional\ 9.0.app/Contents/MacOS/libida32.dylib
```

---

## 5. 放置许可证文件

将 `keygen2.py` 生成的 `idapro.hexlic` 文件复制到你的 home 目录下的 `.idapro` 文件夹：

```bash
mkdir -p ~/.idapro
cp idapro.hexlic ~/.idapro/
```

---

## 6. 启动 IDA Pro 9.0

现在可以正常启动并使用 IDA Pro 9.0 了。

---

**注意事项：**  
- 所有命令均需在终端执行，部分命令（如 `sudo`）需要管理员权限。  
- 若遇到权限或签名问题，确保关闭 SIP 或在恢复模式下操作。
