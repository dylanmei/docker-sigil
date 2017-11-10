docker-sigil
------------

A Docker build for [Sigil](https://github.com/gliderlabs/sigil), a Standalone string interpolator and template processor.

## example

Useful for injecting templates with environment variables.

```
echo 'hello: ${WORLD}' > hello.yaml
docker run --rm -v $PWD:/test -e 'WORLD=earth' sigil -p -f /test/hello.yaml
```

This will output `hello: earth`.
