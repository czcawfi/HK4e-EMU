# hk4e-emu

> HK4E Emulators

## Build binaries

### Quick start

Setup your golang environment, then run the following commands to build binaries.

```bash
$ 设置 golang 环境，然后运行以下命令以生成二进制文件
$ mkdir -p $GOPATH/src/github.com/teyvat-helper
$ cd $GOPATH/src/github.com/teyvat-helper
$ git clone https://github.com/577fkj/hk4e-emu.git
$ cd hk4e-emu
$ go build -trimpath -ldflags "-s -w" -o bin/client cmd/client/main.go
$ go build -trimpath -ldflags "-s -w" -o bin/server cmd/server/main.go
# the binaries are in bin/ directory.
```

Alternatively, use the `go work` command to replace `hk4e-proto` module with your own version.

```bash
$或者，使用该命令将模块替换为您自己的版本。go workhk4e-proto
$ mkdir -p $GOPATH/src/github.com/teyvat-helper
$ cd $GOPATH/src/github.com/teyvat-helper
$ git clone https://github.com/577fkj/hk4e-emu.git
# Place your hk4e-proto directory in the same directory as hk4e-emu.
$ go work init
$ go work use hk4e-emu
$ go work use hk4e-proto
$ cd hk4e-emu
$ go build -trimpath -ldflags "-s -w" -o bin/client cmd/client/main.go
$ go build -trimpath -ldflags "-s -w" -o bin/server cmd/server/main.go
# the binaries are in bin/ directory, with your hk4e-proto.
```
> Note: The `go work` command is only available in Go 1.17 or later.

### Action artifacts

Choose one of the artifacts from the [nightly.link for GitHub](https://nightly.link/):

| Platform              | Arch            | Artifact                                                                                                                      |
|-----------------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------|
| `macOS Intel Chip`    | `darwin/amd64`  | [hke4-emu_darwin_amd64.zip](https://nightly.link/teyvat-helper/hk4e-emu/workflows/build/main/hke4-emu_darwin_amd64.zip.zip)   |
| `macOS Apple Silicon` | `darwin/arm64`  | [hke4-emu_darwin_arm64.zip](https://nightly.link/teyvat-helper/hk4e-emu/workflows/build/main/hke4-emu_darwin_arm64.zip.zip)   |
| `Linux 32 bit`        | `linux/386`     | [hke4-emu_linux_386.zip](https://nightly.link/teyvat-helper/hk4e-emu/workflows/build/main/hke4-emu_linux_386.zip.zip)         |
| `Linux 64 bit`        | `linux/amd64`   | [hke4-emu_linux_amd64.zip](https://nightly.link/teyvat-helper/hk4e-emu/workflows/build/main/hke4-emu_linux_amd64.zip.zip)     |
| `Linux ARM`           | `linux/arm`     | [hke4-emu_linux_arm.zip](https://nightly.link/teyvat-helper/hk4e-emu/workflows/build/main/hke4-emu_linux_arm.zip.zip)         |
| `Linux ARM 64`        | `linux/arm64`   | [hke4-emu_linux_arm64.zip](https://nightly.link/teyvat-helper/hk4e-emu/workflows/build/main/hke4-emu_linux_arm64.zip.zip)     |
| `Windows 32 bit`      | `windows/386`   | [hke4-emu_windows_386.zip](https://nightly.link/teyvat-helper/hk4e-emu/workflows/build/main/hke4-emu_windows_386.zip.zip)     |
| `Windows 64 bit`      | `windows/amd64` | [hke4-emu_windows_amd64.zip](https://nightly.link/teyvat-helper/hk4e-emu/workflows/build/main/hke4-emu_windows_amd64.zip.zip) |
| `Windows ARM`         | `windows/arm`   | [hke4-emu_windows_arm.zip](https://nightly.link/teyvat-helper/hk4e-emu/workflows/build/main/hke4-emu_windows_arm.zip.zip)     |
| `Windows ARM 64`      | `windows/arm64` | [hke4-emu_windows_arm64.zip](https://nightly.link/teyvat-helper/hk4e-emu/workflows/build/main/hke4-emu_windows_arm64.zip.zip) |

## Configuration

## License

[Apache License 2.0](LICENSE)

```
这是java变量
export JAVA_HOME=/usr/lib/java/jdk-17.0.5
export CLASSPATH=$JAVA_HOME/lib:$JRE_HOME/lib:$CLASSPATH
export PATH=$JAVA_HOME/bin:$JRE_HOME/bin:$PATH
export CLASSPATH=$APP_HOME/gradle/wrapper/gradle-wrapper.jar
这是go语言变量 
export GOROOT=/usr/local/go
export GOPATH=/home
export GOBIN=$GOPATH/bin
export PATH=$PATH:$GOROOT/bin
export PATH=$PATH:$GOPATH/bin

执行 刷新  source /etc/profile 
Copyright 2022 Teyvat Helper Team and contributors

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
