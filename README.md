# IonCLI

[![Build Status](https://travis-ci.com/Roger-luo/IonCLI.jl.svg?branch=master)](https://travis-ci.com/Roger-luo/IonCLI.jl)

A CLI package manager for Julia.

**Disclaimer: It’s still at an early stage, even I have tested it myself in daily usage for a few weeks, I still expect it to have some glitches, and please file an issue to help improve it if you hit any.**

For MacOS users, due to system image compilation issue, you will need to compile this package manually via `using IonCLI; IonCLI.comonicon_build()`.

## Installation

<p>
IonCLI is a &nbsp;
    <a href="https://julialang.org">
        <img src="https://julialang.org/favicon.ico" width="16em">
        Julia Language
    </a>
    &nbsp; package. To install IonCLI,
    please <a href="https://docs.julialang.org/en/v1/manual/getting-started/">open
    Julia's interactive session (known as REPL)</a> and press <kbd>]</kbd> key in the REPL to use the package mode, then type the following command
</p>

For stable release

```julia
pkg> add IonCLI
```

For current master

```julia
pkg> add IonCLI#master
```

## Usage

add `~/.julia/bin` to your `PATH`, and type `ion -h` to check help message.

Or you can install paths automatically

```julia
using IonCLI; IonCLI.comonicon_install_path()
```

to install the `PATH` and auto-completion `FPATH` automatically. If you don't have oh-my-zsh installed,
to enable auto-commpletion you need to add `~/.julia/completions` to your `FPATH` and then add 
`autoload -Uz compinit && compinit` to your `.zshrc`.

If you fail to download the artifact, you can build the CLI locally via `IonCLI.comonicon_build()`.

## License

MIT License
