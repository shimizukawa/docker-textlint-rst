textlint-rst
=============

Based upon https://hub.docker.com/r/miy4/textlint/

Docker container with textlint.

### Rules

see https://hub.docker.com/r/miy4/textlint/

### Plugins

This image contains textlint plugins as follows:

- [textlint-plugin-rst](https://www.npmjs.com/package/textlint-plugin-rst)

### Installation

To pull:

```sh
$ docker pull shimizukawa/textlint-rst
```

### Usage

```sh
$ vi .textlintrc
# Edit textlint configurations
```

See [textlint/docs/configuring.md](https://github.com/textlint/textlint/blob/master/docs/configuring.md) and [textlint/examples/config-file/](https://github.com/textlint/textlint/blob/master/examples/config-file) for more details.

For example:

```
{
  "plugins": [
    "rst"
  ],
  "rules": {
    "max-ten": {
      "max": 3
    },
    "spellcheck-tech-word": true,
    "no-mix-dearu-desumasu": true
  }
}
```

Run as
```sh
$ docker run --rm -v ${PWD}:/data -w /data shimizukawa/textlint-rst <TEXTLINT_ARGS>
```

`docker run` accept and pass a set of parameters to [textlint CLI](https://github.com/textlint/textlint#cli).

