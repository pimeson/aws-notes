Fargate is an AWS service that quickly spins up and deploys docker containers without having the need to provision and manage servers.

Each container deployed by fargate is known as a `task`

Deploy Apps not infrastructure: 
- Don't think about patching
- Built in integrations with cloudwatch
	- gather metrics and logs and eventually trigger things such as auto-scaling