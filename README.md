# Caddyfile

Blazing fast HTTPS with [Caddy](https://caddyserver.com/)

```bash
# Test the Caddyfile
sudo caddy -conf ./*.Caddyfile

# Apply
sudo cp ./$HOST.Caddyfile /etc/caddy/caddy.conf
```

## systemd Service for Caddy

> Assume that user `www-data` is already exists.

Make and configure Caddy directories.

```bash
sudo mkdir /etc/caddy
sudo chown -R root:www-data /etc/caddy
sudo mkdir /etc/ssl/caddy
sudo chown -R root:www-data /etc/ssl/caddy
sudo chmod 0770 /etc/ssl/caddy
```

Copy Caddyfile.

```bash
sudo cp ./$HOST.Caddyfile /etc/caddy/Caddyfile
sudo chown www-data:www-data /etc/caddy/Caddyfile
sudo chmod 444 /etc/caddy/Caddyfile
```

Enable the service file

```bash
sudo systemctl enable $PWD/caddy.service
sudo systemctl start caddy
```

## Reference

- https://github.com/pbzweihander/nginx.conf
- https://github.com/simnalamburt/Caddyfile
- https://github.com/mholt/caddy/tree/master/dist/init/linux-systemd
