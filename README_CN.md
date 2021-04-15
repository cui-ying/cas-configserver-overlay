CAS Spring Cloud Configuration Server Overlay Template
============================

通用 CAS Spring Cloud 配置服务器 WAR 覆盖模板。

# 版本

```xml
<cas.version>6.0.x</cas.version>
```

# 需求

* JDK 11

# 构建

要查看该构建脚本有哪些可用命令，运行：
```bash
./build.sh help
```

要打包最终的 web 应用，运行：

```bash
./build.sh package
```

要更新 `SNAPSHOT` 版本，运行：

```bash
./build.sh package -U
```

# 配置

创建文件 `src/main/resources/application.properties` 覆盖默认设置。

# 部署

通过以下方法成功部署后，配置服务器在以下地址可用：

* `https://cas.server.name:8888/casconfigserver`

## 可执行 WAR

以可执行 WAR 运行配置服务器 web 应用。

```bash
./build.sh run
```

## Spring Boot

通过 Spring Boot 以可执行 WAR 运行配置服务器 web 应用。在开发和测试期间最有用。

```bash
./build.sh bootrun
```

## 外部化

部署产生的 `build/libs/casconfigserver.war` （官方给的 target/casconfigserver.war 是针对5.x 的。目前无效了。）到你选择的 servlet 容器。

## 参考
- [我的经验](./my-experience.md)