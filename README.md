# nextjs-aws-cdk-auth-template

This project creates a polyrepo with a frontend writen in NextJS and a Backend connected via routes on AWS ApiGateway. The project is maintained using Github actions to manage the deployment.

1. NextJS

2. Backend

3. DevOps


## DevOps

I have created several github actions 

Create a new feature branch (feature/branch)



## Commands

Resources:
1.  https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/configuring-openid-connect-in-amazon-web-services
2.  https://docs.aws.amazon.com/IAM/latest/UserGuide/id_roles_providers_create_oidc.html

Goto AWS console
Goto IAM
1.  Select Identity Providers
- Add Provider
- OpenId Connect
- Need to enter the Privider / Audience from the github resource link and then click get thumpprint
- Then click add provider to add it.
** Now the AWS token is created **

2.  Now we need to add the permissions for this provider
Click on the provider
Click the Assign Role button (probably in the top right hand corner)
Create new or use existing role
- Web Identity should be selected
- Add the audience (which we entered before )
- Create a policy or use a predefined policy. ** You can even at this stage restrict per repository **









## Resources

https://github.com/jviloria96744/react-aws-cdk-template

mkdir backend
cd backend
cdk init --langugage=typescript

# Hardening GHA to utilise AWS with OpenID
https://docs.github.com/en/actions/deployment/security-hardening-your-deployments/about-security-hardening-with-openid-connect

# GHA - Events that trigger
https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows

# Describes the ci/cd we are trying to create
https://resources.github.com/ci-cd/

# Setup mysql to run in docker
https://github.com/marketplace/actions/setup-mysql
