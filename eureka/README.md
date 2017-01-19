# build and push steps
docker build -t jiglesgom/eureka:latest .
docker login
docker push jiglesgom/eureka