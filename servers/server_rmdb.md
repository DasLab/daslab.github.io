---
permalink: /server_rmdb/
root: /server_rmdb/

title: Server_RMDB
description: "<u>R</u>NA <u>M</u>apping <u>D</u>ata<u>B</u>ase"
repo: DasLab/Server_RMDB
---

# RMDB RNA Mapping DataBase

<img src="https://rmdb.stanford.edu/site_media/images/logo_rmdb.png" alt="RMDB Logo" width="200" align="right">

This is the _Source Code_ repository for **RMDB** RNA Mapping DataBase **Server**. The production server is freely accessible at [https://rmdb.stanford.edu/](https://rmdb.stanford.edu/).

<br/>
<hr/>
## Installation

**RMDB Server** requires the following *Python* packages as dependencies, most of which can be installed through [`pip`](https://pip.pypa.io/).

```js
boto >= 2.38.0
Django >= 1.9.1
django-adminplus >= 0.5
django-crontab >= 0.7.0
django-environ >= 0.4.0
django-filemanager == 0.0.2
django-suit >= 0.2.15
django-widget-tweaks >= 1.4.1
gviz-api.py == 1.8.2
MySQL-python >= 1.2.5
PyGithub >= 1.26.0
pytz >= 2015.7
requests >= 2.9.1
simplejson >= 3.8.1

rdatkit >= 1.0.2
```

* The `rdatkit` package is available internally at [hitrace/rdatkit](https://github.com/hitrace/rdatkit/).

* The `gviz-api.py` is available at [Google/google-visualization-python](https://github.com/google/google-visualization-python/).

* The `django-filemanager` is a modified version of [IMGIITRoorkee/django-filemanager](https://github.com/IMGIITRoorkee/django-filemanager/). The source code is available internally. Install with `sudo python setup.py install`.

* **RMDB Server** also requires proper setup of `imagemagick`, `optipng`, `VARNA.jar`, `mysql.server`, `apache2`, `mod_wsgi`, `openssl`, `gdrive`, `awscli`, and `cron` jobs.

* Lastly, assets preparation is required for the 1st time through running `sudo python manage.py versions`, `sudo python manage.py dist`, `util_prep_dir.sh`, `util_src_dist.sh`, `util_minify.sh`, `util_chmod.sh` and manually replacing `config/*.conf`. For full configuration, please refer to **Documentation**.

<hr/>
## Usage

To run the test/dev server, use:

```bash
cd path/to/server_RMDB/repo
python manage.py runserver
```

<hr/>
## Documentation

- Documentation is available at admin [manual](https://rmdb.stanford.edu/admin/man/) and [reference](https://rmdb.stanford.edu/admin/ref/).

- Alternatively, read the repository [**Wiki**](https://github.com/DasLab/Server_RMDB/wiki/).

<hr/>
## License

**Copyright &copy; 2012-2016: Das Lab, Stanford University. All Rights Reserved.**

**RMDB Server** _Source Code_ is proprietary and confidential. Unauthorized copying of this repository, via any medium, is strictly prohibited.

<hr/>
## Reference

>Cordero, P., *et al.* (**2012**)<br/>
>[An RNA Mapping DataBase for Curating RNA Structure Mapping Experiments.](http://bioinformatics.oxfordjournals.org/content/28/22/3006.long)<br/>
>*Bioinformatics* **28 (22)**: 3006-3008.

README by [**t47**](http://t47.io/), *March 2016*.
