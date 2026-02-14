# XLA ROCm Builds

Prebuilt XLA extension binaries for **x86_64 Linux** with **AMD ROCm** support.

## Releases

See [Releases](https://github.com/team-telnyx/xla-rocm-builds/releases) for available builds.

| Version | ROCm | Platform | Use when |
|---------|------|----------|----------|
| 0.6.0 | 5.7 | x86_64-linux-gnu | Cluster runs ROCm 5.7 (e.g. MI100/gfx908) |
| 0.10.0 | 6.3 | x86_64-linux-gnu | Cluster runs ROCm 6.2+ |

## Usage

Set `XLA_ARCHIVE_PATH` or `XLA_ARCHIVE_URL` in your Elixir/EXLA application.

### ROCm 5.7 (cluster with ROCm 5.7)

```bash
export XLA_ARCHIVE_URL="https://github.com/team-telnyx/xla-rocm-builds/releases/download/v0.6.0-rocm5.7/xla_extension-0.6.0-x86_64-linux-gnu-rocm.tar.gz"
```

### ROCm 6.3 (cluster with ROCm 6.2+)

```bash
export XLA_ARCHIVE_URL="https://github.com/team-telnyx/xla-rocm-builds/releases/download/v0.10.0-rocm/xla_extension-0.10.0-x86_64-linux-gnu-rocm.tar.gz"
```

### Docker

```dockerfile
# ROCm 5.7
ENV XLA_ARCHIVE_URL="https://github.com/team-telnyx/xla-rocm-builds/releases/download/v0.6.0-rocm5.7/xla_extension-0.6.0-x86_64-linux-gnu-rocm.tar.gz"

# ROCm 6.3
ENV XLA_ARCHIVE_URL="https://github.com/team-telnyx/xla-rocm-builds/releases/download/v0.10.0-rocm/xla_extension-0.10.0-x86_64-linux-gnu-rocm.tar.gz"
```

### Local path

```bash
export XLA_ARCHIVE_PATH=/path/to/xla_extension-0.6.0-x86_64-linux-gnu-rocm.tar.gz
```

## Requirements

- Linux x86_64
- AMD GPU with ROCm support (gfx908+)
- ROCm 5.7+ installed (e.g. `ROCM_PATH=/opt/rocm`)

## Cluster compatibility

Tested on `tlnx-backend-at1-dev`:

- **ROCm 5.7:** AMD Instinct MI100 (gfx908)
- **ROCm 6.3:** Same hardware, upgraded runtime

## Source

Built from [elixir-nx/xla](https://github.com/elixir-nx/xla).
