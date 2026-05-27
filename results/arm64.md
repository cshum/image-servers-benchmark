# ARM64

For the public-facing benchmark summary and charts, see the [imagor benchmark docs](https://docs.imagor.net/benchmarks).

Updated 2026-05-28 from detached Singapore AWS rerun.

- AWS server: EC2 `c7g.large` in `ap-southeast-1`
- compared runtimes:
  - imagor: `ghcr.io/cshum/imagor:1.9.1`
  - imgproxy: benchmark harness used `darthsim/imgproxy:latest`; current upstream latest is `ghcr.io/imgproxy/imgproxy:v4.0.3`
  - thumbor: local `benchmark-thumbor:latest`, resolved from `thumbor/Dockerfile` to `thumbor 7.7.7`
- host timestamp: `20260527-181216`
- benchmark shape: `c7g.large`, `2 VUs`, `5m`, `10s` warmup, `512x512`

## JPEG

### imgproxy

```
    checks_total.......: 19895   66.311793/s
    checks_succeeded...: 100.00% 19895 out of 19895
    checks_failed......: 0.00%   0 out of 19895

    ✓ is status 200

    HTTP
    http_req_duration..............: avg=29.86ms min=15.82ms med=29.18ms max=80.58ms p(90)=36.94ms p(95)=40.01ms
      { expected_response:true }...: avg=29.86ms min=15.82ms med=29.18ms max=80.58ms p(90)=36.94ms p(95)=40.01ms
    http_req_failed................: 0.00%  0 out of 19895
    http_reqs......................: 19895  66.311793/s

    EXECUTION
    iteration_duration.............: avg=30.13ms min=16.04ms med=29.45ms max=80.78ms p(90)=37.21ms p(95)=40.3ms 
    iterations.....................: 19895  66.311793/s
    vus............................: 2      min=2          max=2
    vus_max........................: 2      min=2          max=2

    NETWORK
    data_received..................: 854 MB 2.8 MB/s
    data_sent......................: 2.5 MB 8.2 kB/s
```

### thumbor

```
    checks_total.......: 18083   60.272342/s
    checks_succeeded...: 100.00% 18083 out of 18083
    checks_failed......: 0.00%   0 out of 18632

    ✓ is status 200

    HTTP
    http_req_duration..............: avg=32.91ms min=16.97ms med=32.61ms max=67.32ms p(90)=39.75ms p(95)=42.32ms
      { expected_response:true }...: avg=32.91ms min=16.97ms med=32.61ms max=67.32ms p(90)=39.75ms p(95)=42.32ms
    http_req_failed................: 0.00%  0 out of 18083
    http_reqs......................: 18083  60.272342/s

    EXECUTION
    iteration_duration.............: avg=33.16ms min=17.15ms med=32.86ms max=67.51ms p(90)=40.02ms p(95)=42.59ms
    iterations.....................: 18083  60.272342/s
    vus............................: 2      min=2          max=2
    vus_max........................: 2      min=2          max=2

    NETWORK
    data_received..................: 773 MB 2.6 MB/s
    data_sent......................: 2.5 MB 8.3 kB/s
```

### imagor

```
    checks_total.......: 17292   57.634837/s
    checks_succeeded...: 100.00% 17292 out of 17292
    checks_failed......: 0.00%   0 out of 17292

    ✓ is status 200

    HTTP
    http_req_duration..............: avg=34.44ms min=18.79ms med=33.77ms max=81.91ms p(90)=40.85ms p(95)=43.77ms
      { expected_response:true }...: avg=34.44ms min=18.79ms med=33.77ms max=81.91ms p(90)=40.85ms p(95)=43.77ms
    http_req_failed................: 0.00%  0 out of 17292
    http_reqs......................: 17292  57.634837/s

    EXECUTION
    iteration_duration.............: avg=34.68ms min=19.02ms med=34.01ms max=82.66ms p(90)=41.09ms p(95)=44.01ms
    iterations.....................: 17292  57.634837/s
    vus............................: 2      min=2          max=2
    vus_max........................: 2      min=2          max=2

    NETWORK
    data_received..................: 795 MB 2.7 MB/s
    data_sent......................: 2.4 MB 7.9 kB/s
```

## PNG

### imgproxy

```
    checks_total.......: 6194    20.641837/s
    checks_succeeded...: 100.00% 6194 out of 6194
    checks_failed......: 0.00%   0 out of 6194

    ✓ is status 200

    HTTP
    http_req_duration..............: avg=96.6ms  min=34.65ms med=95.59ms max=180.03ms p(90)=117.33ms p(95)=126.14ms
      { expected_response:true }...: avg=96.6ms  min=34.65ms med=95.59ms max=180.03ms p(90)=117.33ms p(95)=126.14ms
    http_req_failed................: 0.00%  0 out of 6194
    http_reqs......................: 6194   20.641837/s

    EXECUTION
    iteration_duration.............: avg=96.86ms min=34.84ms med=95.85ms max=180.21ms p(90)=117.63ms p(95)=126.42ms
    iterations.....................: 6194   20.641837/s
    vus............................: 2      min=2         max=2
    vus_max........................: 2      min=2         max=2

    NETWORK
    data_received..................: 2.0 GB 6.8 MB/s
    data_sent......................: 768 kB 2.6 kB/s
```

### thumbor

```
  checks_total.......: 3731    12.431763/s
  checks_succeeded...: 100.00% 3731 out of 3731
  checks_failed......: 0.00%   0 out of 3731

    ✓ is status 200

    HTTP
    http_req_duration..............: avg=160.59ms min=77.09ms med=160.11ms max=295.05ms p(90)=194.45ms p(95)=209.83ms
      { expected_response:true }...: avg=160.59ms min=77.09ms med=160.11ms max=295.05ms p(90)=194.45ms p(95)=209.83ms
    http_req_failed................: 0.00%  0 out of 3731
    http_reqs......................: 3731   12.431763/s

    EXECUTION
    iteration_duration.............: avg=160.82ms min=77.28ms med=160.29ms max=295.3ms  p(90)=194.65ms p(95)=210.15ms
    iterations.....................: 3731   12.431763/s
    vus............................: 2      min=2         max=2
    vus_max........................: 2      min=2         max=2

    NETWORK
    data_received..................: 1.2 GB 4.1 MB/s
    data_sent......................: 515 kB 1.7 kB/s
```

### imagor

```
    checks_total.......: 6696    22.317409/s
    checks_succeeded...: 100.00% 6696 out of 6696
    checks_failed......: 0.00%   0 out of 6696

    ✓ is status 200

    HTTP
    http_req_duration..............: avg=89.35ms min=34.22ms med=89.17ms max=158.52ms p(90)=107.2ms  p(95)=114ms   
      { expected_response:true }...: avg=89.35ms min=34.22ms med=89.17ms max=158.52ms p(90)=107.2ms  p(95)=114ms   
    http_req_failed................: 0.00%  0 out of 6696
    http_reqs......................: 6696   22.317409/s

    EXECUTION
    iteration_duration.............: avg=89.59ms min=34.4ms  med=89.39ms max=158.74ms p(90)=107.51ms p(95)=114.24ms
    iterations.....................: 6696   22.317409/s
    vus............................: 2      min=2         max=2
    vus_max........................: 2      min=2         max=2

    NETWORK
    data_received..................: 2.9 GB 9.5 MB/s
    data_sent......................: 917 kB 3.1 kB/s
```

## WEBP

### imgproxy

```
    checks_total.......: 7590    25.296551/s
    checks_succeeded...: 100.00% 7590 out of 7590
    checks_failed......: 0.00%   0 out of 7590

    ✓ is status 200

    HTTP
    http_req_duration..............: avg=78.76ms min=34.59ms med=77ms    max=171.96ms p(90)=102.8ms  p(95)=111.09ms
      { expected_response:true }...: avg=78.76ms min=34.59ms med=77ms    max=171.96ms p(90)=102.8ms  p(95)=111.09ms
    http_req_failed................: 0.00%  0 out of 7590
    http_reqs......................: 7590   25.296551/s

    EXECUTION
    iteration_duration.............: avg=79.03ms min=34.96ms med=77.29ms max=172.14ms p(90)=103.04ms p(95)=111.34ms
    iterations.....................: 7590   25.296551/s
    vus............................: 2      min=2         max=2
    vus_max........................: 2      min=2         max=2

    NETWORK
    data_received..................: 237 MB 789 kB/s
    data_sent......................: 956 kB 3.2 kB/s
```

### thumbor

```
  checks_total.......: 6076    20.247153/s
  checks_succeeded...: 100.00% 6076 out of 6076
  checks_failed......: 0.00%   0 out of 6076

    ✓ is status 200

    HTTP
    http_req_duration..............: avg=98.53ms min=55.18ms med=96.69ms max=285.48ms p(90)=119.54ms p(95)=129.72ms
      { expected_response:true }...: avg=98.53ms min=55.18ms med=96.69ms max=285.48ms p(90)=119.54ms p(95)=129.72ms
    http_req_failed................: 0.00%  0 out of 6076
    http_reqs......................: 6076   20.247153/s

    EXECUTION
    iteration_duration.............: avg=98.75ms min=55.36ms med=96.9ms  max=285.7ms  p(90)=119.87ms p(95)=129.98ms
    iterations.....................: 6076   20.247153/s
    vus............................: 2      min=2         max=2
    vus_max........................: 2      min=2         max=2

    NETWORK
    data_received..................: 197 MB 658 kB/s
    data_sent......................: 851 kB 2.8 kB/s
```

### imagor

```
    checks_total.......: 5936    19.781813/s
    checks_succeeded...: 100.00% 5936 out of 5936
    checks_failed......: 0.00%   0 out of 5936

    ✓ is status 200

    HTTP
    http_req_duration..............: avg=100.84ms min=57.62ms med=99.82ms  max=176.86ms p(90)=121.88ms p(95)=132.11ms
      { expected_response:true }...: avg=100.84ms min=57.62ms med=99.82ms  max=176.86ms p(90)=121.88ms p(95)=132.11ms
    http_req_failed................: 0.00%  0 out of 5936
    http_reqs......................: 5936   19.781813/s

    EXECUTION
    iteration_duration.............: avg=101.07ms min=57.82ms med=100.05ms max=177.1ms  p(90)=122.08ms p(95)=132.33ms
    iterations.....................: 5936   19.781813/s
    vus............................: 2      min=2         max=2
    vus_max........................: 2      min=2         max=2

    NETWORK
    data_received..................: 194 MB 646 kB/s
    data_sent......................: 825 kB 2.7 kB/s
```

## AVIF

### imgproxy

```
    checks_total.......: 5807    19.348804/s
    checks_succeeded...: 100.00% 5807 out of 5807
    checks_failed......: 0.00%   0 out of 5807

    ✓ is status 200

    HTTP
    http_req_duration..............: avg=103.07ms min=47.46ms med=101.31ms max=204.57ms p(90)=132.19ms p(95)=143.42ms
      { expected_response:true }...: avg=103.07ms min=47.46ms med=101.31ms max=204.57ms p(90)=132.19ms p(95)=143.42ms
    http_req_failed................: 0.00%  0 out of 5807
    http_reqs......................: 5807   19.348804/s

    EXECUTION
    iteration_duration.............: avg=103.33ms min=47.66ms med=101.57ms max=204.8ms  p(90)=132.45ms p(95)=143.71ms
    iterations.....................: 5807   19.348804/s
    vus............................: 2      min=2         max=2
    vus_max........................: 2      min=2         max=2

    NETWORK
    data_received..................: 184 MB 614 kB/s
    data_sent......................: 732 kB 2.4 kB/s
```

### thumbor

```
  checks_total.......: 5660    18.859944/s
  checks_succeeded...: 100.00% 5660 out of 5660
  checks_failed......: 0.00%   0 out of 5660

    ✓ is status 200

    HTTP
    http_req_duration..............: avg=105.79ms min=47.69ms med=104.58ms max=194.92ms p(90)=135.59ms p(95)=141.51ms
      { expected_response:true }...: avg=105.79ms min=47.69ms med=104.58ms max=194.92ms p(90)=135.59ms p(95)=141.51ms
    http_req_failed................: 0.00%  0 out of 5660
    http_reqs......................: 5660   18.859944/s

    EXECUTION
    iteration_duration.............: avg=106.02ms min=47.87ms med=104.79ms max=195.13ms p(90)=135.78ms p(95)=141.73ms
    iterations.....................: 5660   18.859944/s
    vus............................: 2      min=2         max=2
    vus_max........................: 2      min=2         max=2

    NETWORK
    data_received..................: 223 MB 742 kB/s
    data_sent......................: 792 kB 2.6 kB/s
```

### imagor

```
    checks_total.......: 5742    19.136143/s
    checks_succeeded...: 100.00% 5742 out of 5742
    checks_failed......: 0.00%   0 out of 5742

    ✓ is status 200

    HTTP
    http_req_duration..............: avg=104.26ms min=49.57ms med=102.89ms max=189.18ms p(90)=134.39ms p(95)=145.37ms
      { expected_response:true }...: avg=104.26ms min=49.57ms med=102.89ms max=189.18ms p(90)=134.39ms p(95)=145.37ms
    http_req_failed................: 0.00%  0 out of 5742
    http_reqs......................: 5742   19.136143/s

    EXECUTION
    iteration_duration.............: avg=104.49ms min=49.8ms  med=103.15ms max=189.39ms p(90)=134.63ms p(95)=145.58ms
    iterations.....................: 5742   19.136143/s
    vus............................: 2      min=2         max=2
    vus_max........................: 2      min=2         max=2

    NETWORK
    data_received..................: 227 MB 756 kB/s
    data_sent......................: 798 kB 2.7 kB/s
```
