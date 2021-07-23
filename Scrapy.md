### Get started with Scrapy
https://docs.scrapy.org/en/latest/intro/install.html#intro-install

#### 1. Install framework
```console
pip install Scrapy
```

#### 2. Create new project
```console
scrapy startproject project-name
```

This will create a `project-name` directory with the following contents:

```
project-name
├── scrapy.cfg           # deploy configuration file
├── project-name         # project's Python module, you'll import your code from here
│   └── __init__.py      # project items definition file
│   └── items.py
│   └── middlewares.py   # project middlewares file
│   └── pipelines.py     # project pipelines file
│   └── settings.py      # project settings file
│   └── spiders          # a directory where you'll later put your spiders
│       └── __init__.py
```
