### Get started with Quart
https://pgjones.gitlab.io/quart/tutorials/quickstart.html

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
pip install quart
```

#### 4. Copy initial code to main.py
```python
from quart import Quart

app = Quart(__name__)

@app.route('/')
async def hello():
    return 'hello'

app.run()
```

#### 5. Start server

First option
```console
python hello-world.py
```

Second option
```console
export QUART_APP=hello-world:app
quart run
```

#### 6. Check running server
Open localhost:5000
