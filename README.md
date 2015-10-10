# OpenShift OpenERP quickstart

This quickstart contains an OpenERP installation ready to run on OpenShift.

## Create your app

First, create an application with PostgreSQL:

```
$ rhc app create odoo python-2.7 postgresql-9.2
```

Then, merge and push this repo into your new app. Please be patient, this operation may last for a long time.

```
$ cd odoo/
$ git remote add github https://github.com/jifilis/openshift-odoo-quickstart.git
$ git pull -s recursive -X theirs github master
$ git push
```

That's it!

Now put your own modules in addons dir and do another 
```
git push
```

Now put your own modules in addons dir and do another 
```
git push
```

Point your browser to [https://openerp-$namespace.rhcloud.com](https://openerp-$namespace.rhcloud.com) and login.
Default credentials are:

```
Username: admin
Password: admin
```

## Upgrade

To use master version pull master on previus commands.
