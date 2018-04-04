# Caddyfile

Blazing fast HTTPS with [Caddy](https://caddyserver.com/)

```bash
# Test the Caddyfile
sudo caddy -conf ./*.Caddyfile

# Apply
sudo ln -rsf ./$HOST.Caddyfile /etc/caddy/caddy.conf

# Enable the service file
sudo systemctl enable $PWD/caddy.service
```

## Reference

- https://github.com/pbzweihander/nginx.conf
- https://github.com/simnalamburt/Caddyfile

