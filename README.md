# podman build bug: `COPY` to absolute paths is relative to `WORKDIR`

[issue](https://github.com/containers/buildah/issues/1628)

run in the container:

expected:

```sh
$ cat /bin/foo
foo
```

result:

```sh
$ cat /bin/foo
file not found
$ cat /var/bin/foo
foo
```