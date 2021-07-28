### Get started with Flask

#### 1. Create environment
```console
mkdir myproject
cd myproject
py -3 -m venv venv
```

#### 2. Activate environment
```console
venv\Scripts\activate
```

#### 3. Install Flask
```console
pip install Flask
```

#### 4. Copy initial code to main.py
```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def hello_world():
    return "<p>Hello, World!</p>"
```

#### 5. Start server

CMD
```console
set FLASK_APP=hello
flask run
 * Running on http://127.0.0.1:5000/
```

Bash
```console
export FLASK_APP=hello
flask run
 * Running on http://127.0.0.1:5000/
```

Powershell
```console
$env:FLASK_APP = "hello"
flask run
 * Running on http://127.0.0.1:5000/
```
