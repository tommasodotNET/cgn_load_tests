# Load tests for CGN project

This is a set of [k6](https://k6.io) load tests related to the CGN (carta giovani nazionale) initiative


## Activate new cards based on random "valid" fiscal codes.

You need to set an environment variable `FUNC_KEY` with the azure function app key.

```
docker run -i --rm -v $(pwd)/src:/src  -e FUNC_KEY=${FUNC_KEY} loadimpact/k6 run /src/post_cgn_activation.js
```
