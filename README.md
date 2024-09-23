# ecs-awsdevops-nodeapp  ( https://www.digitalocean.com/community/tutorials/how-to-build-a-node-js-application-with-docker )

1. buildspec file  is user to push the docker image in the repo to ecs


2. so build phase is success using the command in buildspec file
3. no need to create application and Deployment group in code deploy

4.  ecs taskdef and service creted manually using the image uri from ECR and tested the app accesibility using LB endpoint

5. the autodeploy works only when i created an imagedefinition.yml file with  image details

6. now configured a pipeline for auto deploy. please note that in deploy configuration in pipeline  select the ecs details we alredy creted  (Choose buidartifact when giving ecs details in the pipeline configurations)

7. make any changes in the repo and check the source, build and deploy stages. if everything is passed we can verify the working by calling the LB endpoint.
