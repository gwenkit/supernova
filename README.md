# supernova


```
python -m venv venv
grep venv .gitignore
source ./venv/bin/activate
pip install --upgrade pip
pip list
deactivate
```

```
source ./venv/bin/activate
python -m pip install Django
python -m django --version
```

```
django-admin startproject supernova
cd supernova
python manage.py runserver
```

```
python manage.py startapp polls
python manage.py runserver
```

```
brew install postgresql@16
brew services start postgresql@16
echo 'export PATH="/opt/homebrew/opt/postgresql@16/bin:$PATH"' >> ~/.zshrc
createdb supernova
psql supernova
```

```
python manage.py migrate
file db.sqlite3
python manage.py makemigrations polls
python manage.py sqlmigrate polls 0001
python manage.py migrate
```

```
python manage.py createsuperuser
```


