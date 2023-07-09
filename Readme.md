## Setup Go and gin in Linux ubuntu.
# Setup a go project 
```
1. First create a folder and enter it
2. Make a go.mod file that can manage all packages and dependencies. Using this command
    go mod init example/FOLDER_NAME
3. Create file with go extension and type your code and run. 

Happy coding!!
```

# Setup Gin web-frame-work in GoLang projects
```
1. Use above steps to setup project and create a go file.
2. Import gin module or package in your code : import "github.com/gin-gonic/gin"  and then go [build|run|test] will 
   automatically fetch the necessary dependencies. Otherwise, run the following Go command to install the gin package:
    $ go get -u github.com/gin-gonic/gin
3. Run your gin program and test it. This is the demo code.

        package main

        import (
        "net/http"

        "github.com/gin-gonic/gin"
        )

        func main() {
        r := gin.Default()
        r.GET("/ping", func(c *gin.Context) {
            c.JSON(http.StatusOK, gin.H{
            "message": "pong",
            })
        })
        r.Run() // listen and serve on 0.0.0.0:8080 (for windows "localhost:8080")
        }
    
    And use the Go command to run the demo:
        $ go run example.go
        # run example.go and visit 0.0.0.0:8080/ping on browser
    It should be display a msg like this : {"message":"pong"}

Happy Coding!!

```

# Reference for Go installation and Gin setup with demo project
```
Go Install : https://go.dev/doc/install
    - Download go file suitable with your system.
    - For linux --> Remove old go if any :  rm -rf /usr/local/go && tar -C /usr/local -xzf go1.20.5.linux-amd64.tar.gz
    - Extract the archive you just downloaded into /usr/local folder, creating a fresh Go tree in /usr/local/go:
        For Extract : sudo tar -xvzf Downloads/go1.20.5.linux-amd64.tar.gz -C /usr/local/
    - Export the path of Go folder using this command : export PATH=$PATH:/usr/local/go/bin
    - All set now check version : go version 
    Should be display version of go. Like : go version go1.20.5 linux/amd64

Gin setup  : https://go.dev/doc/tutorial/web-service-gin

This helps us to understand things of Go and Gin web framework. 
```