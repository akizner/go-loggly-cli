
# Loggly CLI

  Loggly search command-line tool.

## Installation

  Quick install via go-get:

```
brew install go
go get github.com/segmentio/go-loggly-cli
ln -sf $(go env GOPATH)bin/go-loggly-cli /usr/local/bin
go-loggly-cli --version
```

## Usage

```
go-loggly-cli --help
```

## Examples

```
go-loggly-cli --text --size 100 --account sunbit --user myuser --pass mypass json.kubernetes.container_name:purchase-service OR json.kubernetes.container_name:admin-service
```

## Setup

 Loggly's search API requires basic auth credentials, so you _must_ pass
 the `--acount`, `--user`, and `--pass` flags. To make this less annoying
 I suggest creating an alias:

```sh
alias logs='loggly --account segment --user tj --pass something'
```

 This is a great place to stick personal defaults as well. Since flags are clobbered
 if defined multiple times you can define whatever defaults you'd like here, while
 still changing them via `log`:

```sh
alias logs='loggly --account segment --user tj --pass something --size 5'
```

## License

 MIT
