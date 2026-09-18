# Web key cho xuyen-dem

Chi lay chuc nang, bo UI.

Tren VPS:

```bash
cd /root/xuyen-dem
mkdir -p apps/key-web
cd /tmp
curl -fsSL -o paa https://raw.githubusercontent.com/helloanhem08/xuyen-dem-key-web/main/parts/paa
curl -fsSL -o pab https://raw.githubusercontent.com/helloanhem08/xuyen-dem-key-web/main/parts/pab
curl -fsSL -o pac https://raw.githubusercontent.com/helloanhem08/xuyen-dem-key-web/main/parts/pac
curl -fsSL -o pad https://raw.githubusercontent.com/helloanhem08/xuyen-dem-key-web/main/parts/pad
curl -fsSL -o pae https://raw.githubusercontent.com/helloanhem08/xuyen-dem-key-web/main/parts/pae
cat paa pab pac pad pae | base64 -d > well-known.zip
unzip -o well-known.zip -d /root/xuyen-dem/apps/key-web
ls -la /root/xuyen-dem/apps/key-web
```

File chinh: api.php, manage-keys.php, database.sql, v4-client.php.
