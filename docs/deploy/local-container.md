# Local Container Build and Run

## Build
```bash
docker build -f web/Dockerfile -t ghcr.io/neil795/neil-sinha-it-portfolio:local .
```

## Run
```bash
docker run --rm -p 8080:8080 ghcr.io/neil795/neil-sinha-it-portfolio:local
```

## Smoke check
```bash
curl -I http://127.0.0.1:8080/
```
Expected: `HTTP/1.1 200 OK`
