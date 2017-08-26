# rest-postgres
yet another fullstack node dev't demo

### Requisites (download and install)

* [node](https://nodejs.org/en/download/)
* npm
* [git](https://git-scm.com/downloads)
* [heroku-cli](https://devcenter.heroku.com/articles/heroku-cli)
* [express-generator](https://www.npmjs.com/package/express-generator)
* [stable internet connection](http://beta.speedtest.net/)


### Procedures

* Step 1: Setup Github and Express Server
  * Create new github repo
  * Launch terminal
    ```console
    $ git clone https://github.com/username/repo.git
    $ cd repo
    $ express --view=ejs ./
    $ npm install
    $ npm start
    ```
  * Create file ```.gitignore```    
    ```text
	node_modules
    ```
  * Push to remote repo
  	```console
  	$ git add .
  	$ git config user.email "yourname@example.com"
  	$ git config user.name "yourname"
  	$ git commit -m "initial commit"
  	$ git push origin master
  	```
* Step 2: Deploy to Heroku
  * Verify node version ```$ node --version``` then update ```package.json``` and include engine version.
    ```text
	{
	  "name": "rest-postgres",
	  "version": "0.0.0",
	  "private": true,
	  "scripts": {
	    "start": "node ./bin/www"
	  },
	  "dependencies": {
	    ...
	  },
	  "engines": {
	    "node": "~6.11.2"
	  }
	}
    ```
  * Create file ```.Procfile```
    ```text
    web: npm start
    ```
  * Using heroku cli
    ```console
    $ heroku login
    $ heroku create lastname-repo
    $ git push heroku master
    $ heroku open
    ```

* Step 3: loading...

### References

*[Link 1](https://gigadom.wordpress.com/2014/07/20/working-with-node-js-and-postgresql/)