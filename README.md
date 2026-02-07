# file-receiver

A simple golang server to receive remote files. Needs Tailscale

```
## start the server
go run main.go

## and in a different terminal
tailscale funnel 8080

## and then from the remote machine where you want to send the file from
curl -vXPOST 'https://<TAILSCALE_DOMAIN>/upload' -F "file=@filename.txt"
```

