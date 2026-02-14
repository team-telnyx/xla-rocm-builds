Prebuilt XLA extension for **x86_64 Linux** with **ROCm 6.3**.

## Details
- **Version:** 0.10.0
- **Target:** x86_64-linux-gnu-rocm
- **ROCm:** 6.3
- **Platform:** Linux x86_64 with AMD GPU

## Usage
Set `XLA_ARCHIVE_PATH` or `XLA_ARCHIVE_URL` to this file in your Elixir/EXLA app:

```bash
export XLA_ARCHIVE_URL="https://github.com/team-telnyx/xla-rocm-builds/releases/download/v0.10.0-rocm/xla_extension-0.10.0-x86_64-linux-gnu-rocm.tar.gz"
```

Or in Docker:
```dockerfile
ENV XLA_ARCHIVE_URL="https://github.com/team-telnyx/xla-rocm-builds/releases/download/v0.10.0-rocm/xla_extension-0.10.0-x86_64-linux-gnu-rocm.tar.gz"
```

## Build
Built from [elixir-nx/xla](https://github.com/elixir-nx/xla).
