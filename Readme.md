Kapow tidy example
==================

Sometimes things grow, and keep things tidy it's the only way to mantain the
hole thing.

You can distribute your endpoints among several pow files. And you can keep the
hole thing documented in one html server with kapow.

```
$ cat index.pow
#!/bin/bash

kapow route add / - <<-'EOF'
    cat howto.html | kapow set /response/body
EOF

source ./info_stuff.pow
source ./other_endpoints.pow
```

As you can see the pow files can be imported into another pow files using
source. In fat a pow file it's a regular shell file.

