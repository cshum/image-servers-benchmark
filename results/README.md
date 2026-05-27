# Benchmark Results

Latest canonical release-tag rerun: 2026-05-28 detached AWS benchmark in Singapore.

- region: `ap-southeast-1`
- methodology: `2 VUs`, `5m`, `10s` warmup, `512x512`
- compared runtimes:
	- imagor: `ghcr.io/cshum/imagor:1.9.1`
	- imgproxy: benchmark harness used `darthsim/imgproxy:latest`; current upstream latest is `ghcr.io/imgproxy/imgproxy:v4.0.3`
	- thumbor: local `benchmark-thumbor:latest` built from `thumbor/Dockerfile`; pip resolved `thumbor 7.7.7`, `pillow-avif-plugin 1.5.5`, `pycurl 7.46.0`
- arm64 summary: `results/arm64.md`
- x86_64 summary: `results/x86_64.md`

AWS servers:

- arm64: AWS EC2 `c7g.large` in `ap-southeast-1`, host timestamp `20260527-181216`
- x86_64: AWS EC2 `c7i.large` in `ap-southeast-1`, host timestamp `20260527-181318`

The architecture summary files above are intended to be the readable benchmark docs.