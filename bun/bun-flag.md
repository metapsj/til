# bun --bun flag

Bun respects shebangs. If an executable is marked with `#!/usr/env node`, Bun will
spin up a `node` process to execute the file. However, in some cases it may be desirable to run
executables using Bun's runtime, even if the executable indicates otherwise. To do so, include the
`--bun` flag.

This is also known as the `vite` CLI. The `--bun` flag tells Bun to run Vite's CLI using `bun` instead of
`node`; by default Bun respects Vite's `#!/usr/bin/env node` shebang line.

### examples using the bun and bunx executables

```shell
$ bun --bun run postcss assets/css/app.css -o public/css/app.css
```

```shell
$ bunx --bun my-cli
```
