# DevOpsCorner Docker Container

Docker Container Images Repository for DevOpsCorner.id

### Build Container Image

- Clone this repository

  ```
  git clone https://github.com/devopscorner/devopscorner-container.git
  ```

- Replace "YOUR_AWS_ACCOUNT" with your AWS ACCOUNT ID

  ```
  find ./ -type f -exec sed -i 's/YOUR_AWS_ACCOUNT/123456789012/g' {} \;
  ```

- Execute Build Image

  ```
  make build-cicd-ubuntu
  make build-cicd-alpine
  ```

### Push ECR

- Run this command in terminal:

  ```
  cd compose

  ## Ubuntu
  ./ecr-tag-ubuntu.sh
  ./ecr-push-ubuntu.sh

  ## Alpine
  ./ecr-tag-alpine.sh
  ./ecr-push-alpine.sh
  ```

### Push DockerHub

- Login to your DockerHub Account
- Run this command in terminal:

  ```
  cd compose

  ## Ubuntu
  ./dockerhub-tag-ubuntu.sh
  ./dockerhub-push-ubuntu.sh

  ## Alpine
  ./dockerhub-tag-alpine.sh
  ./dockerhub-push-alpine.sh
  ```

## Copyright

- Author: **Dwi Fahni Denni (@zeroc0d3)**
- Vendor: **DevOps Corner Indonesia (devopscorner.id)**
- License: **Apache v2**
