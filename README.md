# valheim-config

Config for dockerised Valheim dedicated server.

Run `install.sh` to configure:
* Install docker
* Set up `/etc/opt/valheim` to hold config, world saves/backups and such

Then scp in your world from your PC. It is probably in:
`C:\Program Files (x86)\Steam\userdata\56690941\892970\remote\worlds` or `worlds_local`.

But it could also be in `C:\Users\<username>\AppData\LocalLow\IronGate\Valheim\worlds` / `worlds_local`.

Move it onto your VPS, into `/etc/opt/valheim-server/config/worlds_local`.

Run `docker compose up --detach` in the repo root to start the server.

Obviously you need your firewall on the host set up to allow the relevant ports.

## TODOs

* Start via systemd or something idk
* Auto-kill when inactive
* HTTP endpoint to start server
* Actual server management for VPS host

## References
- [Docker image](https://github.com/lloesche/valheim-server-docker)