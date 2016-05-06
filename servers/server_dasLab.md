---
permalink: /server_daslab/
root: /server_daslab/

title: Server_DasLab
description: "Das Lab Website Backend"
repo: DasLab/Server_DasLab
---

# Das Lab Website Server

<img src="https://daslab.stanford.edu/site_media/images/logo_das.jpg" alt="DasLab Logo" align="right">

This is the _Source Code_ repository for **DasLab** Website **Server**. The production server is freely accessible at [https://daslab.stanford.edu/](https://daslab.stanford.edu/).

<br/>
<hr/>
## Installation

**DasLab Server** requires the following *Python* packages as dependencies, most of which can be installed through [`pip`](https://pip.pypa.io/).

```js
boto >= 2.38.0
Django >= 1.9.1
django-adminplus >= 0.5
django-crontab >= 0.7.0
django-environ >= 0.4.0
django-filemanager == 0.0.2
django-suit >= 0.2.15
django-widget-tweaks >= 1.4.1
dropbox >= 4.0
gviz-api.py == 1.8.2
icalendar >= 3.9.1
MySQL-python >= 1.2.5
PyGithub >= 1.26.0
pytz >= 2015.7
requests >= 2.9.1
simplejson >= 3.8.1
slacker >= 0.9.0
```

* The `gviz-api.py` is available at [Google/google-visualization-python](https://github.com/google/google-visualization-python/).

* The `django-filemanager` is a modified version of [IMGIITRoorkee/django-filemanager](https://github.com/IMGIITRoorkee/django-filemanager/). The source code is available internally. Install with `sudo python setup.py install`.

* **DasLab Server** also requires proper setup of `mysql.server`, `apache2`, `mod_wsgi`, `mod_webauth`, `openssl`, `wallet`, `gdrive`, `pandoc`, `awscli`, and `cron` jobs.

* Lastly, assets preparation is required for the 1st time through running `sudo python manage.py versions`, `util_prep_dir.sh`, `util_minify.sh`, `util_chmod.sh` and manually replacing `config/*.conf`. For full configuration, please refer to **Documentation**.

<hr/>
## Usage

To run the test/dev server, use:

```bash
cd path/to/server_daslab/repo
python manage.py runserver
```

<hr/>
## Documentation

- Documentation is available at admin [manual](https://daslab.stanford.edu/admin/man/) and [reference](https://daslab.stanford.edu/admin/ref/).

- Alternatively, read the repository [**Wiki**](https://github.com/DasLab/Server_DasLab/wiki/).

<hr/>
## License

**Copyright &copy; 2015-2016: Das Lab, Stanford University. All Rights Reserved.**

**DasLab Server** _Source Code_ is proprietary and confidential. Unauthorized copying of this repository, via any medium, is strictly prohibited.


README by [**t47**](http://t47.io/), *January 2016*.
