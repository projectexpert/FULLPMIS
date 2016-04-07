Install Instructions on Debian 7
================================

Install system updates
----------------------
```bash
apt-get update && apt-get upgrade
```

Basic setup
-----------
```bash
apt-get install bash-completion nano mc zip unzip arj git mercurial bzr locate
update-alternatives --config editor
```

Create Odoo user
----------------
```bash
adduser --system --quiet --shell=/bin/bash --home=/opt/odoo --gecos 'odoo' --group odoo
```

Install Postgresql set up the postgresql user
--------------------------------------------
```bash
apt-get install postgresql
su - postgres -c "createuser -s odoo" 2> /dev/null || true
```

Install Odoo dependencies
-------------------------
```bash
apt-get install python-imaging python-passlib python-dateutil python-feedparser python-gdata python-ldap python-libxslt1 python-lxml python-mako python-openid python-psycopg2 python-pybabel python-pychart python-pydot python-pyparsing python-reportlab python-simplejson python-tz python-vatnumber python-vobject python-webdav python-werkzeug python-xlwt python-yaml python-zsi python-docutils python-psutil wget python-unittest2 python-mock python-jinja2 python-dev libpq-dev poppler-utils python-pdftools antiword ca-certificates python-six binutils cpp cpp-4.7 gcc-4.7 libgmp10 libgomp1 libitm1 libmpc2 libmpfr4 libquadmath0 python-crypto python-egenix-mxtools python-httplib2 python-keyring python-launchpadlib python-lazr.restfulclient python-lazr.uri python-oauth python-wadllib python-xdg python-zope.interface python-beautifulsoup python-decorator python-requests python-pypdf python-bs4 python-unidecode
```

Install Odoo, project-expert and related repositories
-----------------------------------------------------
```bash
cd /opt
mkdir odoo
cd odoo
git clone https://github.com/projectexpert/FULLPMIS.git
cd FULLPMIS
git submodule init
git submodule update --recursive
git submodule status
```

Update Odoo, project-expert and related repositories
----------------------------------------------------
```bash
cd /opt/odoo&FULLPMIS
git pull
git submodule init
git submodule update --recursive
```

With the newer git versions you can simply:
```bash
git clone --recursive https://github.com/projectexpert/FULLPMIS.git
```

Prepare auto-start
------------------
```bash
sudo cp /opt/odoo/FULLPMIS/odoo-conf/fullpmis-odoo-server /etc/init.d/fullpmis-odoo-server
chmod +x /etc/init.d/fullpmis-odoo-server
service fullpmis-odoo-server start
update-rc.d fullpmis-odoo-server defaults

