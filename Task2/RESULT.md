# Лог тестирования HPA

47m                    Normal    Pulled                    Pod/test-app-deployment-5c977474cc-r2wjb    Successfully pulled image "shestera/scaletestapp" in 1.326s (3.115s including waiting). Image size: 10812245 bytes.
9m8s                   Normal    SuccessfulRescale         HorizontalPodAutoscaler/test-app-hpa        New size: 2; reason: memory resource utilization (percentage of request) above target
9m8s                   Normal    ScalingReplicaSet         Deployment/test-app-deployment              **Scaled up replica set test-app-deployment-5c977474cc from 1 to 2**
9m8s                   Normal    Scheduled                 Pod/test-app-deployment-5c977474cc-xdmb6    Successfully assigned default/test-app-deployment-5c977474cc-xdmb6 to minikube
9m8s                   Normal    SuccessfulCreate          ReplicaSet/test-app-deployment-5c977474cc   Created pod: test-app-deployment-5c977474cc-xdmb6
9m7s                   Normal    Pulling                   Pod/test-app-deployment-5c977474cc-xdmb6    Pulling image "shestera/scaletestapp"
9m5s                   Normal    Created                   Pod/test-app-deployment-5c977474cc-xdmb6    Created container: test-app
9m5s                   Normal    Pulled                    Pod/test-app-deployment-5c977474cc-xdmb6    Successfully pulled image "shestera/scaletestapp" in 2.039s (2.039s including waiting). Image size: 10812245 bytes.
9m5s                   Normal    Started                   Pod/test-app-deployment-5c977474cc-xdmb6    Started container test-app
4m47s                  Normal    Pulled                    Pod/test-app-deployment-5c977474cc-r2wjb    Successfully pulled image "shestera/scaletestapp" in 1.732s (1.732s including waiting). Image size: 10812245 bytes.
3m57s                  Normal    Pulled                    Pod/test-app-deployment-5c977474cc-r2wjb    Successfully pulled image "shestera/scaletestapp" in 1.53s (1.53s including waiting). Image size: 10812245 bytes.
3m5s                   Normal    Pulled                    Pod/test-app-deployment-5c977474cc-r2wjb    Successfully pulled image "shestera/scaletestapp" in 1.668s (1.668s including waiting). Image size: 10812245 bytes.
106s (x5 over 47m)     Normal    Pulling                   Pod/test-app-deployment-5c977474cc-r2wjb    Pulling image "shestera/scaletestapp"
104s                   Normal    Pulled                    Pod/test-app-deployment-5c977474cc-r2wjb    Successfully pulled image "shestera/scaletestapp" in 1.916s (1.916s including waiting). Image size: 10812245 bytes.
104s (x5 over 47m)     Normal    Started                   Pod/test-app-deployment-5c977474cc-r2wjb    Started container test-app
104s (x5 over 47m)     Normal    Created                   Pod/test-app-deployment-5c977474cc-r2wjb    Created container: test-app


user@mk:~/dev$ minikube kubectl -- events
LAST SEEN             TYPE      REASON              OBJECT                                      MESSAGE
60m                   Normal    Pulled              Pod/test-app-deployment-5c977474cc-r2wjb    Successfully pulled image "shestera/scaletestapp" in 1.908s (1.908s including waiting). Image size: 10812245 bytes.
44m                   Normal    SuccessfulCreate    ReplicaSet/test-app-deployment-5c977474cc   Created pod: test-app-deployment-5c977474cc-wt48k
44m                   Normal    Scheduled           Pod/test-app-deployment-5c977474cc-wt48k    Successfully assigned default/test-app-deployment-5c977474cc-wt48k to minikube
44m                   Normal    Pulled              Pod/test-app-deployment-5c977474cc-wt48k    Successfully pulled image "shestera/scaletestapp" in 1.75s (1.75s including waiting). Image size: 10812245 bytes.
42m                   Normal    Pulled              Pod/test-app-deployment-5c977474cc-r2wjb    Successfully pulled image "shestera/scaletestapp" in 1.87s (1.87s including waiting). Image size: 10812245 bytes.
42m                   Normal    Pulled              Pod/test-app-deployment-5c977474cc-xdmb6    Successfully pulled image "shestera/scaletestapp" in 1.322s (2.169s including waiting). Image size: 10812245 bytes.
42m                   Normal    Pulled              Pod/test-app-deployment-5c977474cc-wt48k    Successfully pulled image "shestera/scaletestapp" in 1.336s (1.336s including waiting). Image size: 10812245 bytes.
42m                   Warning   BackOff             Pod/test-app-deployment-5c977474cc-xdmb6    Back-off restarting failed container test-app in pod test-app-deployment-5c977474cc-xdmb6_default(4bec4dbb-b2db-4543-9633-1bfc97c7aa47)
42m                   Warning   BackOff             Pod/test-app-deployment-5c977474cc-wt48k    Back-off restarting failed container test-app in pod test-app-deployment-5c977474cc-wt48k_default(2f80d245-d0e9-4c77-9070-22968576896e)
42m                   Normal    Pulled              Pod/test-app-deployment-5c977474cc-r2wjb    Successfully pulled image "shestera/scaletestapp" in 1.354s (1.354s including waiting). Image size: 10812245 bytes.
42m (x8 over 107m)    Normal    Started             Pod/test-app-deployment-5c977474cc-r2wjb    Started container test-app
42m (x3 over 69m)     Normal    Pulling             Pod/test-app-deployment-5c977474cc-xdmb6    Pulling image "shestera/scaletestapp"
42m (x3 over 44m)     Normal    Pulling             Pod/test-app-deployment-5c977474cc-wt48k    Pulling image "shestera/scaletestapp"
42m (x3 over 69m)     Normal    Created             Pod/test-app-deployment-5c977474cc-xdmb6    Created container: test-app
42m (x3 over 69m)     Normal    Started             Pod/test-app-deployment-5c977474cc-xdmb6    Started container test-app
42m                   Normal    Pulled              Pod/test-app-deployment-5c977474cc-xdmb6    Successfully pulled image "shestera/scaletestapp" in 1.373s (1.373s including waiting). Image size: 10812245 bytes.
42m                   Normal    Pulled              Pod/test-app-deployment-5c977474cc-wt48k    Successfully pulled image "shestera/scaletestapp" in 1.339s (2.712s including waiting). Image size: 10812245 bytes.
42m (x3 over 44m)     Normal    Created             Pod/test-app-deployment-5c977474cc-wt48k    Created container: test-app
42m (x3 over 44m)     Normal    Started             Pod/test-app-deployment-5c977474cc-wt48k    Started container test-app
36m                   Normal    SuccessfulDelete    ReplicaSet/test-app-deployment-5c977474cc   Deleted pod: test-app-deployment-5c977474cc-xdmb6
36m                   Normal    ScalingReplicaSet   Deployment/test-app-deployment              Scaled down replica set test-app-deployment-5c977474cc from 3 to 1
36m                   Normal    Killing             Pod/test-app-deployment-5c977474cc-wt48k    Stopping container test-app
36m                   Normal    SuccessfulDelete    ReplicaSet/test-app-deployment-5c977474cc   Deleted pod: test-app-deployment-5c977474cc-wt48k
36m                   Normal    SuccessfulRescale   HorizontalPodAutoscaler/test-app-hpa        New size: 1; reason: All metrics below target
36m                   Normal    Killing             Pod/test-app-deployment-5c977474cc-xdmb6    Stopping container test-app
32m (x2 over 69m)     Normal    SuccessfulRescale   HorizontalPodAutoscaler/test-app-hpa        New size: 2; reason: memory resource utilization (percentage of request) above target
32m (x2 over 69m)     Normal    ScalingReplicaSet   Deployment/test-app-deployment              Scaled up replica set test-app-deployment-5c977474cc from 1 to 2
32m                   Normal    SuccessfulCreate    ReplicaSet/test-app-deployment-5c977474cc   Created pod: test-app-deployment-5c977474cc-x5wdq
32m                   Normal    Scheduled           Pod/test-app-deployment-5c977474cc-x5wdq    Successfully assigned default/test-app-deployment-5c977474cc-x5wdq to minikube
32m                   Normal    Pulled              Pod/test-app-deployment-5c977474cc-x5wdq    Successfully pulled image "shestera/scaletestapp" in 2.022s (2.022s including waiting). Image size: 10812245 bytes.
32m                   Normal    Pulled              Pod/test-app-deployment-5c977474cc-r2wjb    Successfully pulled image "shestera/scaletestapp" in 1.342s (1.342s including waiting). Image size: 10812245 bytes.
32m (x9 over 107m)    Normal    Created             Pod/test-app-deployment-5c977474cc-r2wjb    Created container: test-app
30m                   Normal    Pulled              Pod/test-app-deployment-5c977474cc-x5wdq    Successfully pulled image "shestera/scaletestapp" in 1.837s (1.837s including waiting). Image size: 10812245 bytes.
30m (x17 over 64m)    Warning   BackOff             Pod/test-app-deployment-5c977474cc-r2wjb    Back-off restarting failed container test-app in pod test-app-deployment-5c977474cc-r2wjb_default(8db9a49f-18ae-4ba3-87af-5a9672755be1)
30m                   Warning   BackOff             Pod/test-app-deployment-5c977474cc-x5wdq    Back-off restarting failed container test-app in pod test-app-deployment-5c977474cc-x5wdq_default(0012b80e-5a06-4e71-b0e7-c3c1b995046f)
30m (x10 over 107m)   Normal    Pulling             Pod/test-app-deployment-5c977474cc-r2wjb    Pulling image "shestera/scaletestapp"
30m (x3 over 32m)     Normal    Pulling             Pod/test-app-deployment-5c977474cc-x5wdq    Pulling image "shestera/scaletestapp"
30m                   Normal    Pulled              Pod/test-app-deployment-5c977474cc-x5wdq    Successfully pulled image "shestera/scaletestapp" in 1.353s (1.353s including waiting). Image size: 10812245 bytes.
30m (x3 over 32m)     Normal    Created             Pod/test-app-deployment-5c977474cc-x5wdq    Created container: test-app
30m (x3 over 32m)     Normal    Started             Pod/test-app-deployment-5c977474cc-x5wdq    Started container test-app
25m                   Normal    SuccessfulCreate    ReplicaSet/test-app-deployment-5c977474cc   Created pod: test-app-deployment-5c977474cc-kd5vx
25m (x2 over 44m)     Normal    ScalingReplicaSet   Deployment/test-app-deployment              Scaled up replica set test-app-deployment-5c977474cc from 2 to 3
25m (x2 over 44m)     Normal    SuccessfulRescale   HorizontalPodAutoscaler/test-app-hpa        New size: 3; reason: memory resource utilization (percentage of request) above target
25m                   Normal    Pulling             Pod/test-app-deployment-5c977474cc-kd5vx    Pulling image "shestera/scaletestapp"
25m                   Normal    Scheduled           Pod/test-app-deployment-5c977474cc-kd5vx    Successfully assigned default/test-app-deployment-5c977474cc-kd5vx to minikube
25m                   Normal    Started             Pod/test-app-deployment-5c977474cc-kd5vx    Started container test-app
25m                   Normal    Pulled              Pod/test-app-deployment-5c977474cc-kd5vx    Successfully pulled image "shestera/scaletestapp" in 1.83s (1.83s including waiting). Image size: 10812245 bytes.
25m                   Normal    Created             Pod/test-app-deployment-5c977474cc-kd5vx    Created container: test-app
2m55s                 Normal    SuccessfulDelete    ReplicaSet/test-app-deployment-5c977474cc   Deleted pod: test-app-deployment-5c977474cc-x5wdq
2m55s                 Normal    ScalingReplicaSet   Deployment/test-app-deployment              Scaled down replica set test-app-deployment-5c977474cc from 3 to 2
2m55s                 Normal    Killing             Pod/test-app-deployment-5c977474cc-x5wdq    Stopping container test-app
2m55s                 Normal    SuccessfulRescale   HorizontalPodAutoscaler/test-app-hpa        New size: 2; reason: All metrics below target



user@mk:~/dev$ minikube kubectl -- get hpa -w
NAME           REFERENCE                        TARGETS           MINPODS   MAXPODS   REPLICAS   AGE
test-app-hpa   Deployment/test-app-deployment   memory: 27%/80%   1         10        2          28m
test-app-hpa   Deployment/test-app-deployment   memory: 44%/80%   1         10        2          28m
test-app-hpa   Deployment/test-app-deployment   memory: 71%/80%   1         10        2          29m
test-app-hpa   Deployment/test-app-deployment   memory: 78%/80%   1         10        2          30m
test-app-hpa   Deployment/test-app-deployment   memory: 91%/80%   1         10        2          31m
test-app-hpa   Deployment/test-app-deployment   memory: 91%/80%   1         10        3          32m
test-app-hpa   Deployment/test-app-deployment   memory: 67%/80%   1         10        3          32m
test-app-hpa   Deployment/test-app-deployment   memory: 60%/80%   1         10        3          33m
test-app-hpa   Deployment/test-app-deployment   memory: 13%/80%   1         10        3          34m
test-app-hpa   Deployment/test-app-deployment   memory: 14%/80%   1         10        3          35m
test-app-hpa   Deployment/test-app-deployment   memory: 15%/80%   1         10        3          36m

^[^C
user@mk:~/dev$ minikube kubectl -- get hpa -w
NAME           REFERENCE                        TARGETS           MINPODS   MAXPODS   REPLICAS   AGE
test-app-hpa   Deployment/test-app-deployment   memory: 15%/80%   1         10        3          39m
test-app-hpa   Deployment/test-app-deployment   memory: 15%/80%   1         10        3          39m
test-app-hpa   Deployment/test-app-deployment   memory: 31%/80%   1         10        1          39m
test-app-hpa   Deployment/test-app-deployment   memory: 31%/80%   1         10        1          40m
test-app-hpa   Deployment/test-app-deployment   memory: 31%/80%   1         10        1          42m
test-app-hpa   Deployment/test-app-deployment   memory: 98%/80%   1         10        1          43m
test-app-hpa   Deployment/test-app-deployment   memory: 98%/80%   1         10        2          44m
test-app-hpa   Deployment/test-app-deployment   memory: 42%/80%   1         10        2          44m
test-app-hpa   Deployment/test-app-deployment   memory: 55%/80%   1         10        2          45m
test-app-hpa   Deployment/test-app-deployment   memory: 22%/80%   1         10        2          46m
test-app-hpa   Deployment/test-app-deployment   memory: 26%/80%   1         10        2          47m
test-app-hpa   Deployment/test-app-deployment   memory: 36%/80%   1         10        2          48m
test-app-hpa   Deployment/test-app-deployment   memory: 74%/80%   1         10        2          49m
test-app-hpa   Deployment/test-app-deployment   memory: 92%/80%   1         10        2          50m
test-app-hpa   Deployment/test-app-deployment   memory: 92%/80%   1         10        3          51m
test-app-hpa   Deployment/test-app-deployment   memory: 64%/80%   1         10        3          51m
test-app-hpa   Deployment/test-app-deployment   memory: 65%/80%   1         10        3          52m
test-app-hpa   Deployment/test-app-deployment   memory: 64%/80%   1         10        3          53m
test-app-hpa   Deployment/test-app-deployment   memory: 64%/80%   1         10        3          54m
test-app-hpa   Deployment/test-app-deployment   memory: 65%/80%   1         10        3          55m
test-app-hpa   Deployment/test-app-deployment   memory: 65%/80%   1         10        3          56m
test-app-hpa   Deployment/test-app-deployment   memory: 65%/80%   1         10        3          57m
test-app-hpa   Deployment/test-app-deployment   memory: 65%/80%   1         10        3          58m
test-app-hpa   Deployment/test-app-deployment   memory: 65%/80%   1         10        3          59m
test-app-hpa   Deployment/test-app-deployment   memory: 65%/80%   1         10        3          60m
test-app-hpa   Deployment/test-app-deployment   memory: 65%/80%   1         10        3          61m
test-app-hpa   Deployment/test-app-deployment   memory: 65%/80%   1         10        3          62m
test-app-hpa   Deployment/test-app-deployment   memory: 64%/80%   1         10        3          63m
test-app-hpa   Deployment/test-app-deployment   memory: 65%/80%   1         10        3          64m
test-app-hpa   Deployment/test-app-deployment   memory: 64%/80%   1         10        3          65m
test-app-hpa   Deployment/test-app-deployment   memory: 61%/80%   1         10        3          66m
test-app-hpa   Deployment/test-app-deployment   memory: 58%/80%   1         10        3          67m
test-app-hpa   Deployment/test-app-deployment   memory: 53%/80%   1         10        3          68m
test-app-hpa   Deployment/test-app-deployment   memory: 44%/80%   1         10        3          69m
test-app-hpa   Deployment/test-app-deployment   memory: 39%/80%   1         10        3          70m
test-app-hpa   Deployment/test-app-deployment   memory: 40%/80%   1         10        3          71m
test-app-hpa   Deployment/test-app-deployment   memory: 40%/80%   1         10        3          72m
test-app-hpa   Deployment/test-app-deployment   memory: 40%/80%   1         10        3          73m
test-app-hpa   Deployment/test-app-deployment   memory: 38%/80%   1         10        2          73m
test-app-hpa   Deployment/test-app-deployment   memory: 31%/80%   1         10        2          74m
test-app-hpa   Deployment/test-app-deployment   memory: 29%/80%   1         10        2          75m
