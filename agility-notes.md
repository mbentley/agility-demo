## Agility - DTR Mirroring/DR with EE
1. Setup Docker EE clusters in two environments; AWS and Azure
2. Enable HRM/Interlock
3. Create demo-aws/docker-demo repo in DTR on AWS
4. Create demo-azure/docker-demo repo in DTR on Azure
5. Create mirroring policy from AWS DTR -> Azure DTR
6. Build an push image to AWS DTR; verify it replicates to Azure
    ```
    docker build -t dtr.aws.demo.dckr.org/demo-aws/docker-demo:latest .
    docker push dtr.aws.demo.dckr.org/demo-aws/docker-demo:latest
    ```
7. Deploy to AWS using client bundle:
docker stack deploy -c docker-compose-aws.yml demo-aws
8. Check app deployed on AWS
http://docker-demo.aws.demo.dckr.org/db
9. Deploy to Azure using client bundle:
docker stack deploy -c docker-compose-azure.yml demo-azure
10. Check app deployed on Azure
http://docker-demo.azure.demo.dckr.org/db
