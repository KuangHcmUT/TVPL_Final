# Deployment
## Create folder
  mkdir datntvpl
  cd datntvpl

## Pull images
  sudo docker pull kanghcmut/lvtn-frontend-app:latest
  sudo docker pull kanghcmut/lvtn-backend-app:latest
  sudo docker pull kanghcmut/lvtn-ai-app:latest

## Git compose
  <!-- One of below -->
  https://github.com/KuangHcmUT/TVPL_Final.git
  git@github.com:KuangHcmUT/TVPL_Final.git
  gh repo clone KuangHcmUT/TVPL_Final

## Crate compose and env files
  sudo nano docker-compose.yml 
   <!-- Add content and save -->
  sudo nano .env
   <!-- Add content and save -->

## Up compose
  sudo docker compose up

## Down compose
  sudo docker compose down

## Login with web_admin
  {
    "email": "qnvn2101@gmail.com",
    "password": "123456Ab"
  }

## Note:
  fe port: 29000
  be port: 29001
  ai port: 29002
  <!-- Expect host -->
  fe host: https://tvpl.thuanle.me 
  be host: https://api-tvpl.thuanle.me
## Install package
  install package if needed inside the Dockerfile