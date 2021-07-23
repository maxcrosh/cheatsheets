### Get started with FastAPI
https://fastapi.tiangolo.com/

##### 1. Install framework
`pip install fastapi`

##### 2. Install webserver
`pip install uvicorn`

##### 3. Copy code to main.py:
```
from fastapi import FastAPI

app = FastAPI()

@app.get("/")
async def root():
    return {"message": "Hello World"}

````
