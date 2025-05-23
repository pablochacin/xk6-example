# xk6-example

**Example k6 extension**

This k6 extension showcases how to develop a k6 JavaScript extension using simple functions. It serves as the basis for new JavaScript extensions created with the `xk6 new` command. Additionally, this repository functions as a GitHub template for creating k6 extension repositories.


```javascript file=script.js
import { greeting } from "k6/x/example";

export default function () {
  console.log(greeting()) // Hello, World!
  console.log(greeting("Joe")) // Hello, Joe!
}
```

For detailed information, refer to the [k6 Extension Development Quick Start Guide](https://github.com/grafana/xk6/wiki/Quick-Start-Guide) and the [k6 Extension Development Tutorial](https://github.com/grafana/xk6/wiki/Tutorial).

## Download

Building a custom k6 binary with the `xk6-example` extension is necessary for its use. You can download pre-built k6 binaries from the [Releases page](https://github.com/grafana/xk6-example/releases/).

## Build

The recommended way to build a custom k6 binary with the `xk6-example` extension is by using the provided Docker image for the [xk6](https://github.com/grafana/xk6) tool.

Linux

```shell
docker run --rm -it -u "$(id -u):$(id -g)" -v "${PWD}:/xk6" grafana/xk6 build --with github.com/grafana/xk6-example
```

macOS

```shell
docker run --rm -it -u "$(id -u):$(id -g)" -v "${PWD}:/xk6" grafana/xk6 build --os darwin --with github.com/grafana/xk6-example
```

Windows (PowerShell)

```
docker run --rm -it -u "$(id -u):$(id -g)" -v "${PWD}:/xk6" grafana/xk6 build --os windows --with github.com/grafana/xk6-example --output k6.exe
```

Windows (cmd.exe)

```
docker run --rm -it -v "%cd%:/xk6" grafana/xk6 build --os windows --with github.com/grafana/xk6-example --output k6.exe
```

## Contribute

If you wish to contribute to this project, please start by reading the [Contributing Guidelines](CONTRIBUTING.md).
