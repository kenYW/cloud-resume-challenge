.PHONY: build

build:
	sam build

deploy-infra:
	sam build && sam deploy

deploy-site:
	aws s3 sync ./resume-site s3://kenyw.com

invoke-put:
	sam build && sam local invoke PutFunction

invoke-get:
	sam build && sam local invoke PutFunction