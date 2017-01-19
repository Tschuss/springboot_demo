# build and push steps
docker build -t jiglesgom/java8:latest .
docker login
docker push jiglesgom/java8