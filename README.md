# Setup
After cloning this repository do the following to setup the prereq environment

- Change to the cloned directory
- From the cli, create a python virtual environment
    
```
python3 -m venv .venv
```

- Activate the newly created virtual environment

```
source .venv/bin/activate
```

- Install the dependencies from the requirements.txt file

```
pip install -r requirements.txt
```

# Run the flask server to serve the example api
- From the cli, Set the following environment variables

```
export FLASK_APP=application.py
export FLASK_ENV=development
```

- If this is the first time you are running this, then initialize the database tables first.

```
flask shell
>>> db.create_all()
>>> quit()
```

- From the cli, run the following command

```
flask run --debug
```