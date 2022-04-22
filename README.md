# cicd-3120-MalachiWissman
- For this project multiple objectives will be completed
	- Containerize an application with Docker
	- Automate the project pipeline with GitHub Actions
	- Explore usage of webhooks to keep production up to date

1. Dockerize it

- how to build the container
	- To start building a container you will need to download docker hub here: https://docs.docker.com/get-docker/.
	- In the setting menu for docker in general tab make sure the box for using the WSL 2 based engine is checked.
	- Now that docker is working for this project i build the container by going to this image guide: https://hub.docker.com/_/httpd.
	- From here the guide lays out instructions ot follow in order to create a container.
- how to run the container
	- To run the container it is also listed in the prevoius guide mentioned but to run a containter you will need to use docker run followed by a set of commands or the image ID.
	- The image ID can be found in docker by using the command $ docker images.
- how to view the project 
	- If you followed the guide properly you can view the project my going to localhost:8080 in your browser to view the project.

2. GitHub Actions and DockerHub

- Create DockerHub public repo
	- Process to create
		- To create a DockerHub repo follow this guide: https://docs.docker.com/docker-hub/repos/.
- How to authenticate with DockerHub via CLI using Dockhub credentials
	- what credentials would you recommend providing?
		- The credientials I recommend providing is your DockerHub username that you created in the previous step and a DockerHub access token.
		- The access token can be created through DockerHub in the account settings and in the security tab.
- Configuring GitHub Secrets
	- what credentials are needed
		- The credentials that are needed is the DockerHub username and the DockerHub access token password.
	- set secrets and secret names
		- To create the github secrets needed follow this guide https://docs.github.com/en/actions/security-guides/encrypted-secrets.
		- When you are creating the secrets you name them DOCKER_USERNAME & DOCKER_PASSWORD respectively.
- Behavior of GitHub workflow
	- what does it do and when
		- the workflow will run everytime something new is puches to the GitHub repo and what it does is run an action that will push docker images to DockerHub.
	- variables to change (repository, etc.)
		- in the workflow you must change the repo name, docker image name, and tag names of your secrets.

3. Deplotment

- Container restart script
	- what it does
		- 
- webhook task defination file
	- what it does
		- 
- Setting up a webhook on the server
	- How you created you own listener
		- 
	- How you installed and are running the webhook on GitHub
		- 
- Setting up a notifier in GitHub or DockerHub
	- 
