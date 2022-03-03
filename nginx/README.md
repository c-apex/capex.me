# NGINX configuration
Certbot is used to manage SSL.

**capex.me** (main) operates in `localhost:3000`

**share.capex.me** (share) operates in `localhost:3001`

For A-Share to allow larger file uploads, `/etc/nginx/nginx.conf` must have `client_max_body_size` under the HTTP section.
e.x.
```
http {
...
client_max_body_size 30M;
}
```

Enable sites by placing them inside `/etc/nginx/sites-available/` and running this command:
`ln -s /etc/nginx/sites-available/capex.me.conf /etc/nginx/sites-enabled/`