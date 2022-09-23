### Docker
- List Images : `docker images`
- List all containers : `docker ps -a`
- Remove containers : `docker rm <id>`
- Remove image : `docker rmi <image name>`
- Run interective mode with overiding entry point : `docker run --rm -it --entrypoint /bin/sh <image name>`

### Docker Compose
- Run specific image : `docker-compose up -d --build website`
- Remove container after execution : `docker-compose run --rm --build unit-tests`
- Validate and view compose file : `docker-compose config`
- Just build an image : `docker-compose build <service name>`
- Distroy : `docker-compose distory`

### Terraform
- Initialize : `terraform init`
- View plan : `terraform plan`
- Apply : `terraform apply`
- View cashed output : `terraform output`

### AWS cli
- List S3 buckets : `aws s3 ls`
- List S3 bucket content : `aws s3 ls --recursive s3://melearning.tk`
- Copy to S3 bucket : `aws s3 cp --recursive website/ s3://melearning.tk`
- Remove all content : `aws s3 rm s3://melearning.tk --recursive`