### Get started with Express
https://expressjs.com/ru/starter/generator.html

#### 1. Install express-generator app globaly
```console
npm install express-generator -g
```

#### 2. Run generator to create a project folder
```console
express --view=ejs myapp
   
   create : myapp
   create : myapp/package.json
   create : myapp/app.js
   create : myapp/public
   create : myapp/public/javascripts
   create : myapp/public/images
   create : myapp/routes
   create : myapp/routes/index.js
   create : myapp/routes/users.js
   create : myapp/public/stylesheets
   create : myapp/public/stylesheets/style.css
   create : myapp/views
   create : myapp/views/index.pug
   create : myapp/views/layout.pug
   create : myapp/views/error.pug
   create : myapp/bin
   create : myapp/bin/www
```

#### 3. Install requirements
```console
cd myapp
npm install
```

#### 4. Run localhost

MacOS & Linux
```console
DEBUG=myapp:* npm start
```

Windows
```console
set DEBUG=myapp:* & npm start
```

#### 5. In the browser open
http://localhost:3000/ 
