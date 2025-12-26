# http-debug-proxy

> MITM-style proxy to debug HTTP based services

`http-debug-proxy` passes HTTP requests to the provided endpoint, and logs both
requests and responses as Markdown files per request.

## Usage

```bash
NAME=my_debug_session_name PROXY_PORT=9000 ENDPOINT=http://localhost:8000 deno run --allow-env --allow-net --allow-write jsr:@thrudhame/http-debug-proxy
```

- `NAME`: namespace/subfolder to group request files in.
- `PROXY_PORT`: Port number for proxy to listen to.
- `ENDPOINT`: URL for the endpoint to debug.

<!--deno-fmt-ignore-start-->
> [!NOTE]
> It will create `debug` folder to put all the subfolders and request files into.
<!--deno-fmt-ignore-end-->
