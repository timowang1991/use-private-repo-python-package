# What is this?

* This is a demonstration of how we can add python packages from an unpublished private github repo.

* In Pipfile
```
[packages]
my-private-module-package = {git = "https://${GITHUB_PERSONAL_ACCESS_TOKEN}@github.com/timowang1991/private-repo-python-package.git"}
```

<br/><br/>

# Installation Caveats

## How to install a new private repo package to a new `Pipfile` file

```
PERSONAL_ACCESS_TOKEN=<your_personal_access_token>

pipenv install git+https://${PERSONAL_ACCESS_TOKEN}@github.com/timowang1991/private-repo-python-package.git#egg=my_private_module_package
```


<br/><br/>

## How to install with existing `Pipfile`

* Create `.env` from `.env.example`, and add your [personal access token](https://github.com/settings/tokens) into `.env`
```
cp .env
```

* Install
```
pipenv shell
pipenv install
```

<br/><br/>

# How to run this repo

* Create `.env` from `.env.example`, and add your [personal access token](https://github.com/settings/tokens) into `.env`
```
cp .env
```

* Run command
```
docker-compose up
```

<br/><br/>

# References
* [Installing Private Python Packages](https://docs.readthedocs.io/en/stable/guides/private-python-packages.html)
* [Support for Environment Variables](https://pipenv-fork.readthedocs.io/en/latest/advanced.html#support-for-environment-variables)
