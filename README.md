<!--
https://readme42.com
-->


[![](https://img.shields.io/pypi/v/django-configurations-installed-apps.svg?maxAge=3600)](https://pypi.org/project/django-configurations-installed-apps/)
[![](https://img.shields.io/badge/License-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)
[![](https://github.com/andrewp-as-is/django-configurations-installed-apps.py/workflows/tests42/badge.svg)](https://github.com/andrewp-as-is/django-configurations-installed-apps.py/actions)

### Installation
```bash
$ [sudo] pip install django-configurations-installed-apps
```

#### Features
key  | default value  | env
-|-|-
`INSTALLED_APPS_FILE` | `None` | `DJANGO_INSTALLED_APPS_FILE`
`INSTALLED_APPS_FILES` | `[]` | `DJANGO_INSTALLED_APPS_FILES`
`INSTALLED_APPS_DISCOVER` | `True` | `DJANGO_INSTALLED_APPS_DISCOVER`  ('yes', 'y', 'true', '1')

##### `settings.py`
```python
from configurations import Configuration
from django_configurations_installed_apps import InstalledAppsMixin

class Base(InstalledAppsMixin,Configuration):
    INSTALLED_APPS_FILE = 'apps.txt'
    INSTALLED_APPS_DISCOVER = True
```

`apps.txt`
```
django.contrib.admin
django.contrib.auth
django.contrib.contenttypes
django.contrib.sessions
django.contrib.messages
django.contrib.sites
django.contrib.staticfiles

django_gravatar
```

#### Links
+   [django-configurations](https://github.com/jazzband/django-configurations)
+   [django-discover-apps](https://pypi.org/project/django-discover-apps/)

<p align="center">
    <a href="https://readme42.com/">readme42.com</a>
</p>
