# go-cups 

> Experimental Golang bindings for CUPS

## Info

This is an experimental library that provides limited bindings to CUPS. 

Currently only working on OS X and can print files

## Usage

```shell
go get https://github.com/vopi181/gcups
```

## Example

```go
package main

import (
    "fmt"

    cups "github.com/vopi181/gcups"
)

func main() {
    printers := cups.NewDefaultConnection()
    for _, dest := range printers.Dests {
        fmt.Printf("%v (%v)\n", dest.Name, dest.Status())
    }
    dest[0].PrintFile("/tmp/test.txt", "Hello From The Otherside")

}
```

## Credits

Forked from ![adrianfallerio's go-cups](https://github.com/adrianfalleiro/go-cups)
