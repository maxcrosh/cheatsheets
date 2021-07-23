### Get started with Scrapy
https://docs.scrapy.org/en/latest/intro/install.html#intro-install

#### 1. Install framework
```pip install Scrapy```

#### 2. Create new project
```scrapy startproject project-name```

This will create a `project-name` directory with the following contents:
```
tutorial/
    scrapy.cfg            # deploy configuration file

    tutorial/             # project's Python module, you'll import your code from here
        __init__.py

        items.py          # project items definition file

        middlewares.py    # project middlewares file

        pipelines.py      # project pipelines file

        settings.py       # project settings file

        spiders/          # a directory where you'll later put your spiders
            __init__.py
```
