# Go Project Template

This repository provides a simple way to generate a clean Go project structure automatically.

## Features

- Creates the recommended directory structure for Go projects.
- Adds common files like `go.mod`, `.gitignore`, and `Makefile`.
- Use the project name and username provided to build templates files.
- The LICENSE file is dynamically generated.

## Usage

1. Clone this repository:

```
$ bash git clone https://github.com/yourusername/go-project-template.git
$ cd go-project-template
```

2. Run the script to create a new project:

```
$ ./create-project.sh <my-go-project> [username] [license]
```

If the second and third parameters are not provided, the following strings will be used by default:

* username:
    * Default value: username
* license:
    * Options available: Apache-2.0, GPL-3.0 or MIT.
    * Default value: MIT

3. Navigate to your project directory:

```
$ cd my-go-project
```

4. Initialize Go modules and start coding:

```
$ go mod tidy
```

## Structure

The generated project will have the following structure:

```
my-go-project/
├── cmd/
│   └── server/
│       └── main.go       # Entry point for the application
├── configs/
│   └── config.yaml       # Configuration file
├── internal/
│   ├── server/
│   │   └── server.go     # Server implementation
│   └── handlers/
│       └── handler.go    # Example HTTP handler
├── pkg/
│   └── utils/
│       └── logger.go     # Reusable utility for logging
├── scripts/
│   └── build.sh          # Automation script to build the project
├── test/
│   └── integration_test.go # Basic integration test
├── .gitignore
├── docker-compose.yml
├── Dockerfile
├── go.mod
├── LICENSE
├── Makefile
└── README.md
```

## How It Works

1. Build the project:

Run the build script or use the Makefile.

```$ make build```

2. Run the server:

Start the application.

```$ make run```

3. Testing:

Execute the tests to ensure everything works as espected.

```$ make test```

4. Configurations:

Update the config/config.yml file to modify parameters like the server port or database settings.