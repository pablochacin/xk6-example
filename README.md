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

Use the [xk6](https://github.com/grafana/xk6) tool to build a custom k6 binary with the `xk6-example` extension. Refer to the [xk6 documentation](https://github.com/grafana/xk6) for more information.

## Contribute

If you wish to contribute to this project, please start by reading the [Contributing Guidelines](CONTRIBUTING.md).
