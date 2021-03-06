# Asynqmon

Asynqmon is a web based tool for monitoring and administrating Asynq queues and tasks.

## Compatibility

Current version of Asynqmon is compatible with [Asynq v0.15 or above](https://github.com/hibiken/asynq/releases).

## Installation

### Release binaries

You can download the release binary for your system from the
[releases page](https://github.com/hibiken/asynqmon/releases).

### Building from source

To build Asynqmon from source code, first ensure that have a working
Go environment with [version 1.16 or greater installed](https://golang.org/doc/install).
You also need [Node.js](https://nodejs.org/) and [Yarn](https://yarnpkg.com/)
installed in order to build the frontend assets.

Download the source code and then run:

```sh
$ make build
```

The `asynqmon` binary should be created in the current directory.

## Usage

Asynqmon server needs to connect to redis server to serve data.
By default, it connects to redis server running on port 6379 locally, and the server listens on port 8080.

To use the defaults, simply run and open http://localhost:8080.

```sh
$ asynqmon
```

Pass flags to specify port, redis server address, etc.

```sh
$ asynqmon --port=3000 --redis_addr=localhost:6380
```

To see all available flags, run

```sh
$ asynqmon --help
```

## License

Asynqmon is released under the MIT license. See [LICENSE](https://github.com/hibiken/asynqmon/blob/master/LICENSE).
