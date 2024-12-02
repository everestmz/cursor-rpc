# cursor-rpc

Protos and go library to communicate with Cursor's backend, without using Cursor. Useful if you're only allowed to run proprietary code through the Cursor servers/have a paid Cursor license, but want to use your own editor (Vim, Helix, etc) or build other features on top of Cursor.

Works by reverse-engineering the minified, obfuscated JS in Cursor's VSCode fork and acting like a bootleg module loader to stand up only the relevant modules needed to get the Protobuf typing info.

## Usage

TODO

## Updating the schema

To update the schema, run

```console
make extract-schema
```

This command assumes you have a `Cursor.app` in your `/Applications` directory.

Then, run

```console
make generate
```

To use `buf` to generate updated Go bindings for cursor-rpc.


## Todos

- auto-generate the `cursor_version.txt` (currently manually set)
- auto-updating when Cursor has new releases
- more testing & examples
