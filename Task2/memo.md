# Memo of HPA lab


## Run test-pod
```
minikube kubectl -- apply -f load2.yml
minikube kubectl -- exec -ti test-pod -- bash
apt update
apt install iputils-ping
apt install iproute2
pip install locust
```

## Url for locust

http://10.105.187.110:8080


## Create locustfile
```
cat <<EOF > locustfile.py
> from locust import HttpUser, between, task
class WebsiteUser(HttpUser):
    wait_time = between(1, 5)
    @task
    def index(self):
        self.client.get("/")
> EOF
```

## Run locust
```
root@test-pod:/# locust 
[2025-03-16 15:57:48,464] test-pod/INFO/locust.main: Starting Locust 2.33.2
[2025-03-16 15:57:48,465] test-pod/INFO/locust.main: Starting web interface at http://0.0.0.0:8089, press enter to open your default browser.
```

## NAT for locust
```
minikube kubectl -- port-forward pod/test-pod 8089:8089
```