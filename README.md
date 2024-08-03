# supernova


## development

```
cd supernova
source ./venv/bin/activate
python manage.py migrate
python manage.py shell
python manage.py test
deactivate
```

### once(ready)

```
git clone https://github.com/gwenkit/supernova.git
cd supernova
pyenv local 3.12.4
python -m venv venv
grep venv .gitignore
source ./venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
pip list
cd supernova
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
deactivate
```


## log

### once(env)

```
pyenv local 3.12.4
cd supernova
python -m venv venv
grep venv .gitignore
source ./venv/bin/activate
pip install --upgrade pip
source ./venv/bin/activate
python -m pip install Django
python -m django --version
pip freeze > requirements.txt
```

### once(startproject)

```
django-admin startproject supernova
cd supernova
python manage.py runserver
```

### startapp

```
python manage.py startapp polls
python manage.py runserver
```

### once(postgres)

```
brew install postgresql@16
brew services start postgresql@16
echo 'export PATH="/opt/homebrew/opt/postgresql@16/bin:$PATH"' >> ~/.zshrc
createdb supernova
psql supernova
```

### once(sqlite)

```
python manage.py migrate
file db.sqlite3
```

### createsuperuser

```
python manage.py createsuperuser
```

### migrate

```
python manage.py makemigrations polls
python manage.py sqlmigrate polls 0001
python manage.py migrate
```

### test

```
python manage.py shell
python manage.py test polls
```


