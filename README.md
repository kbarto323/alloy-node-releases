# alloy-node Releases

Public download host for **alloy-node**, the unified Go agent for
[alloy-router](https://github.com/kbarto323/alloy-router) (private source).
The agent runs on hosts that own AI backends and/or IP cameras and reports
state to a central core.

## Download

Grab the archive for your platform from the [Releases page](https://github.com/kbarto323/alloy-node-releases/releases/latest):

| OS | Architecture | Archive |
|---|---|---|
| macOS | Apple Silicon | `alloy-node_vX.Y.Z_Darwin_arm64.tar.gz` |
| macOS | Intel | `alloy-node_vX.Y.Z_Darwin_x86_64.tar.gz` |
| Linux | x86_64 | `alloy-node_vX.Y.Z_Linux_x86_64.tar.gz` |
| Linux | arm64 | `alloy-node_vX.Y.Z_Linux_arm64.tar.gz` |
| Windows | x86_64 | `alloy-node_vX.Y.Z_Windows_x86_64.zip` |

Each archive contains the `alloy-node` binary, a `node.yaml.example`
config template, and the project README.

Verify integrity against `checksums.txt`:

```
sha256sum -c checksums.txt --ignore-missing
```

> **About the "Source code" downloads.** GitHub adds "Source code (zip)"
> and "Source code (tar.gz)" links to every release page automatically
> — there's no way to hide them. They contain *only this README*; the
> actual alloy-node source lives in the private
> [alloy-router](https://github.com/kbarto323/alloy-router) repo and is
> not distributed here. Use the binary archives in the asset list above.

## Quick start

```
tar -xzf alloy-node_*_Darwin_arm64.tar.gz
cp node.yaml.example node.yaml   # edit core_url + api_key
./alloy-node
```

**macOS Gatekeeper**: first run will be blocked. Bypass with:

```
xattr -dr com.apple.quarantine alloy-node
```

## What's in this repo

This repo holds release tags + binaries only. There is no source code
here. Issue tracking and source live in the private repo.