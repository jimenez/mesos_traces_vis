This assumes all the tracing data is installed into a local redis instance.

###To ingest local data into redis:

```shell
$ tail -f -c +1 <path> | python -u populate_trace_db.py
```

###To compile Go binary:

```shell
$ go get -u
$ go build
```

##T#o start services

Start the redis server (default localhost on port 6379)

Start Go server (default 0.0.0.0 on port 3000)

```shell
$ ./mesos_traces_vis -p <port> -r <redis ip:port>
```

Access traces at http://<ip>:<port>




