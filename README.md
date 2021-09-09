# Redis Commands Schema

This is the schema for Redis' Commands JSON documents. It is based on the design proposed in [_"A better approach for COMMAND INFO for movablekeys commands #8324"_](https://github.com/redis/redis/pull/8324) and [_"Redis as the SSOT of its commands #9359"_](https://github.com/redis/redis/issues/9359).

This project contains the following directories:

* `schema`: the JSON schema
* `commands`: sample command JSONs

## Development quickstart

1. Install a JSON Schema Validator, e.g.:
    ```sh
    go get github.com/neilpa/yajsv
    ```

2. Run a webserver from the `schema` directory, e.g.:
    ```sh
    cd schema
    python -m SimpleHTTPServer 80
    ```

3. Execute from the project's root:
   ```sh
   yajsv -s schema/commands.schema.json commands/*
   ```
