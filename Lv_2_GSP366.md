# Level 2 
# GSP366

## Step 1 || Run on VM instance

### Replace ```<dynamic-VM_NAME>``` with ur VM Name & ```<dynamic-VM_ZONE>``` with ur Zone
```bash
gcloud compute ssh <dynamic-VM_NAME> --zone <dynamic-VM_ZONE>
```
```bash
export DOCKER_TAG=gcr.io/ql-shared-resources-test/defect_solution@sha256:776fd8c65304ac017f5b9a986a1b8189695b7abbff6aa0e4ef693c46c7122f4c
export VISERVING_CPU_DOCKER_WITH_MODEL=${DOCKER_TAG}
export HTTP_PORT=8602
export LOCAL_METRIC_PORT=8603
```
```bash
docker pull ${VISERVING_CPU_DOCKER_WITH_MODEL}
```
### Replace ```<dynamic-CONTAINER_NAME>``` 
```bash
docker run -v /secrets:/secrets --rm -d --name <dynamic-CONTAINER_NAME> \
 
GSP366
--network="host" \
-p ${HTTP_PORT}:8602 \
-p ${LOCAL_METRIC_PORT}:8603 \
-t ${VISERVING_CPU_DOCKER_WITH_MODEL}
```

## Check Progress for Task 1 Before moving to remaining task
## Remaining Tasks || Run on Cloud Shell
```bash
export CONTAINER_NAME=
```
```bash
export TASK_3_FILE_NAME=
```
```bash
export TASK_4_FILE_NAME=
```
```bash

curl -LO raw.githubusercontent.com/quiccklabs/Labs_solutions/master/Detect%20Manufacturing%20Defects%20using%20Visual%20Inspection%20AI%20Challenge%20Lab/quicklabgsp366.sh

sudo chmod +x quicklabgsp366.sh

./quicklabgsp366.sh


```