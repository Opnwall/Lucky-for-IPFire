# Lucky for IPFire

This project adds a Lucky management entry to the IPFire WebUI.

Lucky provides DDNS, ACME certificate management, port forwarding, web services,
scheduled tasks and other router-focused tools.

## Included Runtime

- Lucky `v2.27.2`
- Source release: `https://github.com/gdy666/lucky/releases/tag/v2.27.2`
- Asset: `lucky_2.27.2_Linux_x86_64.tar.gz`
- SHA256: `78adf3fa5e8869be0b1510cb7bcc755d57dccb13252989c8394a7207a392fe66`

The bundled binary is installed to:

```text
/opt/lucky/bin/lucky
```

Lucky configuration is stored in:

```text
/var/ipfire/lucky/conf
```

## Install

Copy the project directory to IPFire, then run as `root`:

```sh
cd "lucky for IPFire"
chmod +x install.sh uninstall.sh src/etc/rc.d/init.d/lucky src/srv/web/ipfire/cgi-bin/lucky.cgi src/opt/lucky/bin/lucky
./install.sh
```

Open the IPFire WebUI and go to:

```text
Services > Lucky
```

The default Lucky address is:

```text
https://IPFire-address:16601/
```

Default Lucky login:

```text
Username: 666
Password: 666
```

Change the password and set a secure access path immediately after first login.

## Service

```sh
/etc/rc.d/init.d/lucky start
/etc/rc.d/init.d/lucky stop
/etc/rc.d/init.d/lucky restart
/etc/rc.d/init.d/lucky status
```

## Uninstall

```sh
cd "lucky for IPFire"
./uninstall.sh
```

The uninstaller removes the service, WebUI page, menu entry and runtime files.
Configuration data remains in `/var/ipfire/lucky/conf`.
