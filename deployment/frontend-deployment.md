# Frontend Deployment Workflow

## Build Frontend Project

```bash
npm run build
```

## Common Build Error

### Problem

Build failed because of dependency conflict.

### Solution

Delete the following file:

```text
node_modules/icore-sdk/node_modules/file-saver/FileSaver.js
```

---

# Docker Image Deployment

## Pull Base Image

```bash
docker pull registry.example.com/project/frontend:1.1.0.1
```

## Generate Dockerfile

```bash
echo "from registry.example.com/project/frontend:1.1.0.1" > Dockerfile
```

## Remove Existing Nginx Files

```bash
echo "RUN rm -rf /usr/share/nginx/html/*" >> Dockerfile
```

## Copy Frontend Files

```bash
echo "COPY dist/ /usr/share/nginx/html/" >> Dockerfile
```

## Build Image

```bash
docker build -t registry.example.com/project/frontend:v1.1.0.1 .
```

## Push Image

```bash
docker push registry.example.com/project/frontend:v1.1.0.1
```
