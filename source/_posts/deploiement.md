---
title: deploiement
date: 2017-07-14 18:40:31
tags:
---

on dit que le meilleur site sur ce sujet :
[How to setup a blog on github with Hexo]
(https://zirho.github.io/2016/06/04/hexo/)


https://hexo.io/docs/deployment.html
Deployment
Hexo provides a fast and easy deployment strategy. You only need one single command to deploy your site to your servers.

$ hexo deploy
Before your first deployment, you will have to modify some settings in _config.yml. A valid deployment setting must have a type field. For example:

deploy:
  type: git
You can use multiple deployers. Hexo will execute each deployer in order.

deploy:
- type: git
  repo:
- type: heroku
  repo:
Git
Install hexo-deployer-git.

$ npm install hexo-deployer-git --save
Edit settings.

deploy:
  type: git
  repo: <repository url>
  branch: [branch]
  message: [message]
Option	Description
repo	GitHub/Bitbucket/Coding/GitLab repository URL
branch	Branch name. The deployer will detect the branch automatically if you are using GitHub or GitCafe.
message	Customize commit message (Default to Site updated: {{ now('YYYY-MM-DD HH:mm:ss') }})
Heroku
Install hexo-deployer-heroku.

$ npm install hexo-deployer-heroku --save
Edit settings.

deploy:
  type: heroku
  repo: <repository url>
  message: [message]
Option	Description
repo, repository	Heroku repository URL
message	Customize commit message (Default to Site updated: {{ now('YYYY-MM-DD HH:mm:ss') }})
Rsync
Install hexo-deployer-rsync.

$ npm install hexo-deployer-rsync --save
Edit settings.

deploy:
  type: rsync
  host: <host>
  user: <user>
  root: <root>
  port: [port]
  delete: [true|false]
  verbose: [true|false]
  ignore_errors: [true|false]
Option	Description	Default
host	Address of remote host	
user	Username	
root	Root directory of remote host	
port	Port	22
delete	Delete old files on remote host	true
verbose	Display verbose messages	true
ignore_errors	Ignore errors	false
OpenShift
Install hexo-deployer-openshift.

$ npm install hexo-deployer-openshift --save
Edit settings.

deploy:
  type: openshift
  repo: <repository url>
  message: [message]
Option	Description
repo	OpenShift repository URL
message	Customize commit message (Default to Site updated: {{ now('YYYY-MM-DD HH:mm:ss') }})
FTPSync
Install hexo-deployer-ftpsync.

$ npm install hexo-deployer-ftpsync --save
Edit settings.

deploy:
  type: ftpsync
  host: <host>
  user: <user>
  pass: <password>
  remote: [remote]
  port: [port]
  ignore: [ignore]
  connections: [connections]
  verbose: [true|false]
Option	Description	Default
host	Address of remote host	
user	Username	
pass	Password	
remote	Root directory of remote host	/
port	Port	21
ignore	Ignore the files on either host or remote	
connections	Connections number	1
verbose	Display verbose messages	false
SFTP
Install [hexo-deployer-sftp]. Deploys the site via SFTP, allowing for passwordless connections using ssh-agent.

$ npm install hexo-deployer-sftp --save
Edit settings.

deploy:
  type: sftp
  host: <host>
  user: <user>
  pass: <password>
  remotePath: [remote path]
  port: [port]
  privateKey: [path/to/privateKey]
  passphrase: [passphrase]
  agent: [path/to/agent/socket]
  remotePath: [remotePath]
Option	Description	Default
host	Address of remote host	
user	Username	
pass	Password	
remotePath	Root directory of remote host	/
port	Port	22
privateKey	Path to a ssh private key	
passphrase	Optional passphrase for the private key	
agent	Path to the ssh-agent socket	$SSH_AUTH_SOCK
Other Methods
All generated files are saved in the public folder. You can copy them to wherever you like.

