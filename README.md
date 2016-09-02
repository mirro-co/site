# Mirroco Official Website

The website for mirro.co

## Getting started to setup static blog using github pages + hexo

1. Install [git](https://git-scm.com/downloads) & [node.js](https://nodejs.org/en/download/) on your local computer

2. Create two repositories on github.com
 
	```
	repo name: mirro-co.github.io
	purpose: store generated & deployed hexo site pages (hexo public directory)

	repo name: site
	purpose: store the hexo source for the site
	```

3. Setup ssh key so that no password required for every login, check [this](https://help.github.com/categories/ssh/) 
	```
	NOTE: if you installed TortoiseSVN, GIT_SSH will be set to TortoisePlink.exe, it's better to unset it to use ssh from git bash
	```
	
4. Install Hexo
	```bash
	$ npm install hexo-cli -g
	$ npm install hexo-deployer-git -g
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
	$ npm install hexo-deployer-git --save
	```
	
	Add addtional themes
	```bash
	$ git clone git://github.com/tommy351/hexo-theme-phase.git themes/phase
	```
	
	Change themes to phase in _config.yml
	```yaml
	theme: phase
	```
	
	Generate static pages, static pages will be generated under 'public' directory,
	```bash
	$ hexo generate
	```
	Start hexo server to view the blog locally
	```bash
	$ hexo server
	```

	view the blog on http://localhost:4000
	

6. Push the hexo site to github repository 'site'
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
	$ cd site
	$ hexo new "your post name"
	```
	
	a markdown file will be generated in source/_posts/your post name.md, edit this file with a markdown supported text editor 
	
	view the blog on http://localhost:4000

8. Deploy the generated static blog site to github pages
	```bash
	$ hexo deploy
	```

## Getting started to create & post a blog

1. Clone the repository to your local folder
	```bash
	$ git clone https://github.com/mirro-co/site.git
	```
