# Deployment

Move to branch **_deploy_**

For the arm architecture, move to branch: **_arm-deploy_**

## Clone docker compose repository

```
sudo git clone --branch arm-deploy https://github.com/KuangHcmUT/tvpl-deploy.git

cd tvpl-deploy
```

Change the branch name if needed

## Verify Docker Compose File

```
cat docker-compose.yml
```

## Crate env file and add content

```
sudo nano .env
```

### BE

**MONGODB_URI**: Uri connect to the database contain the database name

**AI_HOST**: AI service running host

**JWT_SECRET**: Secret string when generating jwt token

### FE

**NEXTAUTH_URL**: Web client call web server for authentication

**NEXT_SERVER_API_HOST**: Web server call BE API server

**NEXT_PUBLIC_API_HOST**: Web client call BE API server

**API_HOST**: Is like the NEXT_PUBLIC_API_HOST, when NEXT_PUBLIC_API_HOST is inaccessible

## Pull and deploy images

```
sudo docker compose up
```

## AI service compose

### Move to AI folder

```
cd AI
```

### Verify Docker Compose File

```
cat docker-compose.yml
```

### Crate env file and add content

```
sudo nano .env
```

**DATABASE_URI**: Uri connect to the database without the database name

**DATABASE_NAME**: The database name

### Pull and deploy images

```
sudo docker compose up
```

# Login with web with admin role after deploy successfully

```
  {
    "email": "qnvn2101@gmail.com",
    "password": "123456Ab"
  }
```

# Note:

## Port:

    fe port: 29000

    be port: 29001

    ai port: 29002

## Expect host

    fe host: https://pl.thuanle.me

    be host: https://api-pl.thuanle.me
