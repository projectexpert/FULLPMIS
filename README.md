Unified Odoo Addons Repository
==============================

You have to add your destination's ssh key to both, GitLab and Github accounts!

```bash
git clone git@github.com:projectexpert/FULLPMIS.git

git submodule init

git submodule update --recursive

git submodule status

```

Git update

```bash
git pull

git submodule init

git submodule update --recursive
```

With the newer git versions you can simply:

```bash
git clone --recursive git@github.com:projectexpert/FULLPMIS.git
```

Example addon path (if your odoo user's home, where you clone the repo is /opt/openerp):

```bash
addons_path = /opt/openerp/FULLPMIS/__base__/odoo/addons,/opt/openerp/fullodoo/__other__/project-expert,/opt/openerp/FULLPMIS,/opt/openerp/FULLPMIS/__oca__/account-financial-reporting,/opt/openerp/FULLPMIS/__oca__/account-financial-tools,/opt/openerp/FULLPMIS/__oca__/account-invoicing,/opt/openerp/FULLPMIS/__oca__/connector-telephony,/opt/openerp/FULLPMIS/__oca__/crm,/opt/openerp/FULLPMIS/__oca__/event,/opt/openerp/FULLPMIS/__oca__/hr-timesheet,/opt/openerp/FULLPMIS/__oca__/knowledge,/opt/openerp/FULLPMIS/__oca__/management-system,/opt/openerp/FULLPMIS/__oca__/manufacturing,/opt/openerp/FULLPMIS/__oca__/odoomrp-wip,/opt/openerp/FULLPMIS/__oca__/partner-contact,/opt/openerp/FULLPMIS/__oca__/product-attribute,/opt/openerp/FULLPMIS/__oca__/project-service,/opt/openerp/FULLPMIS/__oca__/purchase-workflow,/opt/openerp/FULLPMIS/__oca__/reporting-engine,/opt/openerp/FULLPMIS/__oca__/sale-workflow,/opt/openerp/FULLPMIS/__oca__/server-tools,/opt/openerp/FULLPMIS/__oca__/social,/opt/openerp/FULLPMIS/__oca__/web,/opt/openerp/FULLPMIS/__oca__/website
```
