This is a clean Django project template to get you started quickly. The template includes config Systemd, nginx, gunicorn.

Installation is just specifying the Python interpreter and domain name, run:

```bash
./install.sh
```

In the Django config, fill in the database settings (`src/config/settings.py`).

View the status of the gunicorn daemon:

```bash
sudo systemctl status gunicorn
```

Gunicorn's logs are in `gunicorn/access.log` и `gunicorn/error.log`.

After changing the systemd config, you need to re-read it and then restart the unit:

```bash
sudo systemctl daemon-reload
sudo systemctl restart gunicorn
```
