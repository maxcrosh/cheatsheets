### Get started with FastAPI
https://fastapi.tiangolo.com/


#### 1. Install framework
```console
pip install fastapi
```


#### 2. Install web server
```console
pip install uvicorn
```


#### 3. Copy code to main.py:
```python
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def root():
    return {"message": "Hello World"}

````


#### 4. Run web server
```console
uvicorn main:app --reload
```
