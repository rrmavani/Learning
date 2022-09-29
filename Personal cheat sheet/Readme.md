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

### Kubernets
- View kubectl version `kubectl version --client --output=yaml`
- View kubectl configuration `kubectl config view`
- Use kubectl with specific config file `kubectl --kubeconfig config get nodes`
- View cluster information `kubectl config get-clusters`
- Force kubectl to use specific config file `export KUBECONFIG="<path>"`
- Force kubectl to use localhost config `unset $KUBECONFIG`

<br>

- View kubectl nodes `kubectl get nodes`
- View pod in details `kubectl describe pod first-pod`
- View services `kubectl get services`
- View nodes `kubectl get nodes`
- View deployments `kubectl get deployments`
- View all resources `kubectl get all`
- View a bit more details `-o wide` ex `kubectl get pods -o wide`
- View specific details `-o=custom-columns=NAME:.metadata.name,STATUS:.status.phase,NODE:.spec.nodeName`

<br>

- Apply configuration `kubectl apply -f pod.yml`
- Delete some resources or objects `kubectl delete pod.yml`
- Scale deployment to specific replicas `kubectl scale replicas=5 deployments/qsk-deploy`

<br>

- Port forwaring of node-port service `kubectl port-forward --address 0.0.0.0 service/cloud-lb 8080:8080`
