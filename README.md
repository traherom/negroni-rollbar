# negroni-rollbar
A negroni middleware for rollbar

Forked from [jfbus/negroni-rollbar](https://github.com/jfbus/negroni-rollbar) simply because I didn't want to have it
configure Rollbar internally.

The middleware forwards all panics to rollbar.com.

```
import "github.com/traherom/negroni-rollbar"

func main() {
  n := negroni.Classic()
  n.Use(rollbar.Report())
}
```

rollbar.Report recovers panics, the default Recovery handler does nothing.
