# Linkedin Learning Course
## Devops Foundations: Your First Project
##### by Carlos Nunez

- [Create Image using Dockerfile and docker-compose](Create_image_docker_docker-compose.md)
- [Test with rspec capybara selenium](rspec_capybara_selenium.md)
- If you removed your images and containers, Run below to run and test your so far.
    - Run website `docker-compose up -d --build website `
    - Access and verify it with **http://localhost**
    - Run selenium container `docker-compose up -d --build selenium`
    - Open tigervnc and connect to `localhost:5900`
    - Run test `docker-compose run --rm unit-tests`

- [Run terraform in Docker](terraform_in_docker.md)
- [Create S3 bucket using terraform](Create_s3_bucket.md)
- [Deploy website to S3 (awscli in docker)](deploy_website_S3.md)