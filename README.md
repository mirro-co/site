# Mirroco Official Website

The website for mirro.co

## Getting started to setup static blog using github pages + hexo

1. Install [git](https://git-scm.com/downloads) & [node.js](https://nodejs.org/en/download/) on your local computer

2. Create a repository on github.com
 
	```
	repo name: mirro-co.github.io
	purpose: for deployed hexo site pages

	repo name: site
	purpose: for the hexo site source
	```

3. Setup ssh key so that no password required for every login, check [this](https://help.github.com/categories/ssh/) 

4. Install Hexo
	```bash
	$ npm install hexo-cli -g
	```
	
5. Initiate blog under directory 'site'
	
   Initiate the site
	```bash
	$ hexo init site
	```
	
	Install the dependencies in the local node_modules folder
	```bash
	$ cd site 
	$ npm install
	```
	
	change the themes
	```bash
	$ git clone git://github.com/tommy351/hexo-theme-phase.git themes/phase
	```
	
	change themes to phase in _config.yml
	
	generate static pages and review
	```bash
	$ hexo generate
	```
	static pages will be generated under 'public' directory, start hexo server
	```bash
	$ hexo server
	```
	
	view the blog on http://localhost:4000
	

6. Deploy to github repository 'site'
	```bash
	$ cd site
	$ git init
	$ git add .
	$ git commit -m "first commit"
	$ git remote add origin https://github.com/mirro-co/site.git
	$ git push -u origin master
	```
	
7. Create a new post and start hexo server to view your blog locally	[http://localhost:4000]
	```bash
	$ cd blog
	$ hexo new "your post name"
	```
	
	a markdown file will be generated in source/_posts/your post name.md, edit this file using a text editor 
	which supports markdown (sublime text)
	
	view the blog on http://localhost:4000
	

8. Deploy the blog to github pages



## Getting started to create & post a blog

1. Clone the repository to your local folder
	```bash
	$ git clone https://github.com/mirro-co/site.git
	```
