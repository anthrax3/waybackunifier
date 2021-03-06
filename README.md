# WaybackUnifier

WaybackUnifier allow you to take a look at how a file has ever looked by aggregating all versions of this file, and creating a unified version that contains every line that has ever been in it.

### Installation
Go is required.
```
go get github.com/mhmdiaa/waybackunifier
cd $GOPATH/src/github.com/mhmdiaa/waybackunifier
go install
```

### Syntax
```
  -concurrency int
        Number of requests to make in prallel (default 1)
  -output string
        File to save results in (default "output.txt")
  -sub string
        list of comma-separated substrings to look for in snapshots (snapshots will only be considered if they contnain one of them) (default "Disallow,disallow")
  -url string
        URL to unify versions of (without protocol prefix) (default "site.com/robots.txt")
```

You can see that settings are by default suitable for unifying robots.txt files. Feel free to change the value of `-sub` to anything else, or supply an empty string to get all versions of a file without filtering.

**Note:** Lines are saved *unordered* for performance reasons