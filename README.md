# Stringer

A small CLI for transforming and inspecting strings, built with Go and [Cobra](https://github.com/spf13/cobra).

I built `stringer` as an example to explain and showcase Cobra. You can read the full article [on my blog](https://thorsten-hans.com/lets-build-a-cli-in-go-with-cobra/).

## Requirements

- Go 1.25 or newer

## Installation

```bash
go install github.com/ThorstenHans/stringer@latest
```

Or build from source:

```bash
git clone https://github.com/ThorstenHans/stringer.git
cd stringer
go build -o stringer .
```

## Usage

### Reverse a string

```bash
stringer reverse "Hello, Gopher"
# rehpoG ,olleH
```

Alias: `rev`

### Inspect a string

Counts the characters in a string:

```bash
stringer inspect hello
# 'hello' has 5 chars.
```

Use `--digits` (`-d`) to count only digits:

```bash
stringer inspect -d abc123
# 'abc123' has 3 digits.
```

Alias: `insp`

### Other commands

- `stringer --version`: print the version
- `stringer completion <shell>`: generate a shell completion script (bash, zsh, fish, powershell)
- `stringer help [command]`: show help for any command

## Project layout

```
.
├── main.go                # entry point
├── cmd/stringer/          # Cobra commands (root, reverse, inspect)
└── pkg/stringer/          # string logic used by the commands
```

## License

[MIT](LICENSE)
