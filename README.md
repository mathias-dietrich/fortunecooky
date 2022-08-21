# fortunecooky
Rest service to create random fortune cookies in Python on Kubernetes

build:
docker build -f Dockerfile -t fortunecooky:latest .
docker tag fortunecooky matd/fortunecooky
docker push matd/fortunecooky

deploy
kubectl apply -f deployment.yaml

re-eploy:
kubectl rollout restart deploy fortunecooky