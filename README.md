# README

This is the Public [Guidebolt](https://guidebolt.com/) Knowledge-Base

[Changelog](https://k.guidebolt.com/changelog/)

## Read Online

[https://k.guidebolt.com/](https://k.guidebolt.com/)

## Read Locally

```

cd ~

git clone https://github.com/Guidebolt/knowledge.git

cd knowledge/

sudo pip install mkdocs mkdocs-material

mkdocs serve

```

[http://127.0.0.1:8000/](http://127.0.0.1:8000/)

## Create Static Website

```

cd ~

git clone https://github.com/Guidebolt/knowledge.git

cd knowledge/

sudo pip install mkdocs mkdocs-material

mkdocs build --clean

(the above command generates static site files at ~/knowledge/site)

```

Data files are archived separately at [https://k.guidebolt.com/files/latest-archive.zip](https://k.guidebolt.com/files/latest-archive.zip). Download and extract to the folder at ~/knowledge/files.

```

Copy static site files to "/srv/site" of hosting server

Copy data files to "/srv/files" of hosting server

```

NGINX web server dual-folder config snippet:

```

location /files {
	root /srv;
	try_files $uri $uri/ =404;
}

location / {
	root /srv/site;
    try_files $uri $uri/ =404;
}


```

## Updates

mkdocs, mkdocs-material

```
# one time setup of python virtual environment
python3 -m python-venv

# activate virtual environment
source python-venv/bin/activate

mkdocs --version

pip install -U mkdocs

pip install -U mkdocs-material
```

merging update branch into main branch

```
git checkout master

git merge --squash readybranchnamehere
```

## Dependencies

Markdown to Static Site Converter: [https://www.mkdocs.org/](https://www.mkdocs.org/)

Visual Theme: [https://squidfunk.github.io/mkdocs-material/](https://squidfunk.github.io/mkdocs-material/)

TLS Certificates: [https://letsencrypt.org/](https://letsencrypt.org/)

