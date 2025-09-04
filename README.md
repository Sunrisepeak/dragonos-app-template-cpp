# dragonos-app-template-cpp

DragonOS的C++模板项目 - 支持自动配置DragonOS环境, 程序的安装和内核运行

---

<details>
  <summary>点击查看xlings安装命令</summary>

---

#### Linux

```bash
curl -fsSL https://d2learn.org/xlings-install.sh | bash
```

#### Windows - PowerShell

```bash
Invoke-Expression (Invoke-Webrequest 'https://d2learn.org/xlings-install.ps1.txt' -UseBasicParsing).Content
```

> 注: xlings具备多版本共存的包管理功能 -> [详情](https://d2learn.org/xlings)

---

</details>

### 添加DragonOS包索引仓库

> 项目所需的依赖的包索引

```bash
xim --add-indexrepo dragonos:https://github.com/sunrisepeak/xim-pkgindex-dragonos.git
xim --update index
```

### 安装该模板项目

> 这里会自动配置好需要运行的环境(第一次安装依赖可能需要一些时间), 安装成功后即可在当前目录看到模板项目的目录名helloworld
>
> 会自动安装以下依赖:
>
> - [dragonos-dev](https://github.com/Sunrisepeak/xim-pkgindex-dragonos/blob/main/pkgs/d/dragonos-dev.lua): DragonOS开发环境
> - [dragonos-tool](https://github.com/Sunrisepeak/xim-pkgindex-dragonos/blob/main/pkgs/d/dragonos-tool.lua): DragonOS辅助工具(dotool)
> - [musl-gcc](https://github.com/d2learn/xim-pkgindex/blob/main/pkgs/m/musl-gcc.lua): C/C++编译器(基于musl-libc)
>

```bash
xlings new helloworld --template dragonos:app-template-cpp
```

<img width="1171" height="772" alt="Image" src="https://github.com/user-attachments/assets/7c34d3c3-bffc-4d1f-a13d-8983d0af70c1" />

### 基本用法

> **d2x**为xlings的项目辅助构建工具, 模板项目的程序名默认为`helloworld`, 详情见`config.xlings`

- **d2x build**: 构建该项目
- **d2x run**: 在本地运行项目构建的程序
- **d2x install**: 安装项目的程序到DragonOS的内核镜像中(默认为/bin目录)
- **d2x run-kernel**: 运行内核(可以在内核文件系统中找到安装的程序并运行测试)

## 其他

- xpkg包文件: https://github.com/Sunrisepeak/xim-pkgindex-dragonos/blob/main/pkgs/a/app-template-cpp.lua
- DragonOS: https://github.com/DragonOS-Community/DragonOS
- DragonOS包索引仓库: https://github.com/Sunrisepeak/xim-pkgindex-dragonos
- xlings包管理器: https://github.com/d2learn/xlings
- 问题反馈和技术交流: https://forum.d2learn.org/category/9/xlings