# taskq

A simple task queue. :-)

## Usage:

Get the package like this:

```sh

go get -u -v github.com/sfshf/taskq

```

Use the task queue like this:

```go

q := taskq.RunQ(context.Background(), 10, 100)
defer q.ShutD(0)

t := taskq.NewT("simple task queue", func(v interface{}) {
    fmt.Printf("hello, %s\n", v)
})
q.Push(t)


```
