
Install
---

    $ npm install component-hooks

Usage
---

### component.json (local component)
---

```
{
  "name": "app",
  "jade": [
    "templates/index"
  ],
  "styl": [
    "style"
  ],
  "coffee": [
    "index",
    "collections",
    "views"
  ]
}
```

### server.coffee

```
hooks = require 'component-hooks'

express = require 'express'
app = express()

app.get '/', hooks, (req, res) ->
  res.render 'index'

port = process.env.PORT || 3000
app.listen port, ->
  console.log "http://dev:#{port}"
```

Example
---

    $ make example