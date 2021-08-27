# mlflow-tracking-server
Docker infrastructure to deploy a MLflow tracking server with MYSQL datastore backend

# Setup
You need a `.env` file with the following variables:
```bash
MYSQL_DATABASE="<>"
MYSQL_USER="<>"
MYSQL_PASSWORD="<>"
MYSQL_ROOT_PASSWORD="<>"
MLFLOW_VOLUME="<>"
```

`MLFLOW_VOLUME` is used a shared folder between the container and the host to
ensure persistance. Many examples of this setup use s3 storage, but when it
comes to Local File Storage, you need a shared folder, a shared volume wouldn't
allow for the python API to correctly save artifacts (e.g.: folder won't
exist).

# Disclosure
This server is unprotected and publicly available, if you need security just
put it behind a proxy.

# License
MIT License

Copyright (c) 2021 Guillermo Blanco

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
