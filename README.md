[![Software License](https://img.shields.io/badge/license-MIT-brightgreen.svg?style=flat-square)](/LICENSE)
[![Build status](https://github.com/hoto/template-go-cli/workflows/Build%20and%20test/badge.svg?branch=master)](https://github.com/hoto/template-go-cli/actions)
[![Release](https://img.shields.io/github/release/hoto/template-go-cli.svg?style=flat-square)](https://github.com/hoto/template-go-cli/releases/latest)
[![Powered By: goreleaser](https://img.shields.io/badge/powered%20by-goreleaser-green.svg?style=flat-square)](https://github.com/goreleaser/goreleaser)

# Golang application template repository

Clone and replace `template-go-cli` with the name of your project.

Github action will use `goreleaser` to automatically releases formula to homebrew repo at [hoto/homebrew-repo](https://github.com/hoto/homebrew-repo) on every git tag.

### Installation
    
Mac:

    brew install hoto/homebrew-repo/template-go-cli

Mac or Linux:

    sudo curl -L \
      "https://github.com/hoto/template-go-cli/releases/download/1.0.3/template-go-cli_1.0.3_$(uname -s)_$(uname -m)" \
       -o /usr/local/bin/template-go-cli

    sudo chmod +x /usr/local/bin/template-go-cli
    
Or manually download binary from [releases](https://github.com/hoto/template-go-cli/releases).
    
### Run

    template-go-cli --help
    template-go-cli --version
    template-go-cli
    
### Development

Build and test:

    go get github.com/hoto/template-go-cli
    
    make dependencies build test
    
Build binary:

     make build
    ./bin/template-go-cli

Run with arguments:

    make args="myargs" run

Install to global golang bin directory:

    make install
    template-go-cli
    
### Release

Add a git tag and push it to GH. 
GH action will pick it up and goreleaser will publish to https://github.com/hoto/homebrew-repo