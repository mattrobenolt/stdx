# Moved to baskingspot/stdx

This repository is archived. stdx lives at [baskingspot/stdx](https://github.com/baskingspot/stdx), with its full history. The guide is at https://baskingspot.dev/stdx/.

This repository stopped at commit `87db8fa`. The module name is unchanged.

## Migrate

Fetch it from the new location:

```sh
zig fetch --save git+https://github.com/baskingspot/stdx
```

Your `build.zig` stays the same:

```zig
const stdx = b.dependency("stdx", .{ .target = target, .optimize = optimize });
exe.root_module.addImport("stdx", stdx.module("stdx"));
```

If another package depends on the old URL, its `build.zig.zon` needs the new `.url` and `.hash`. Run `zig fetch --save` there too.
