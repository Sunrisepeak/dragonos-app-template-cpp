# dragonos-app-template-cpp

DragonOS的C++模板项目 - 支持自动配置DragonOS环境, 程序的安装和内核运行

## 添加DragonOS包索引仓库

```bash
xim --add-indexrepo dragonos:https://github.com/sunrisepeak/xim-pkgindex-dragonos.git
xim --update index
```

## 安装该模板项目

> 这里会自动配置好需要运行的环境(第一次运行需要一些时间)
> - dragonos-dev
> - dragonos-tool
> - musl-gcc

```bash
xlings install dragonos:app-template-cpp
```

## 基本用法

> 程序的默认名为`helloworld`, 详情见`config.xlings`

- **d2x build**: 构建该项目
- **d2x run**: 在本地运行项目构建的程序
- **d2x install**: 安装项目的程序到DragonOS的内核镜像中(默认为/bin目录)
- **d2x run-kernel**: 运行内核(然后可以在内核文件系统中找到百年写的程序并运行测试)

## 其他

- DragonOS: https://github.com/DragonOS-Community/DragonOS
- DragonOS包索引仓库: https://github.com/Sunrisepeak/xim-pkgindex-dragonos
- xlings包管理器: https://github.com/d2learn/xlings