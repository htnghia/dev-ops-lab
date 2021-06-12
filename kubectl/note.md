## scale kubectl
$ kubectl scale --replicas 5 deployment calculator-deployment

## Deploy service wihout yml file
kubectl expose deployment order-service-deployment --type=LoadBalancer --port=6060

## create tunnel for service using minikube
minikube service order-service

## test order service curl
curl --location --request GET 'http://127.0.0.1:30240/api/v1/order?page=0&size=2&sort=desc&sortBy=createdDate' --header 'Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJzdWIiOiIxMjM0NTY3ODkwIiwidXNlcklkIjoiZXJ3cjM0NTM0ZmdlZnJld3IiLCJpYXQiOjE1MTYyMzkwMjJ9.yy6RNHz1oL24eJlYCeU7Z3fzAIa_vrHLi9zLpj3clLE'