## nocache

nocache is a simple piece of middleware that sets a number of HTTP headers to prevent a router (or subrouter) from being cached by an upstream proxy and/or client.  

[![GoDoc](https://godoc.org/github.com/things-go/nocache?status.svg)](https://godoc.org/github.com/things-go/nocache)
[![Go.Dev reference](https://img.shields.io/badge/go.dev-reference-blue?logo=go&logoColor=white)](https://pkg.go.dev/github.com/things-go/nocache?tab=doc)
[![Build Status](https://travis-ci.org/things-go/nocache.svg)](https://travis-ci.org/things-go/nocache)
[![codecov](https://codecov.io/gh/things-go/nocache/branch/master/graph/badge.svg)](https://codecov.io/gh/things-go/nocache)
![Action Status](https://github.com/things-go/nocache/workflows/Go/badge.svg)
[![Go Report Card](https://goreportcard.com/badge/github.com/things-go/nocache)](https://goreportcard.com/report/github.com/things-go/nocache)
[![Licence](https://img.shields.io/github/license/things-go/nocache)](https://raw.githubusercontent.com/things-go/nocache/master/LICENSE)
[![Tag](https://img.shields.io/github/v/tag/things-go/nocache)](https://github.com/things-go/nocache/tags)


## Usage

### Start using it

Download and install it:

```bash
    go get github.com/things-go/nocache
```

Import it in your code:

```go
    import "github.com/things-go/nocache"
```

### Example

```go
package main

import (
	"github.com/gin-gonic/gin"

	"github.com/things-go/nocache"
)

func main() {
	router := gin.Default()
	gin.Use(nocache.NoCache())
	router.Run(":8080")
}
```
