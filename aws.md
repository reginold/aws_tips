#### AWS EFS 関連技術

- 失败了为什么container不删除呢 dockeropertoter
- [fstabについて](https://qiita.com/kihoair/items/03635447591358210772)


#### AWS Datasync 関連技術
- s3,efsなら、`aws sync xx xx` CLIでもよい
- オンプレなら、datasyncの方が良い
- Amazon S3 Glacier または Amazon S3 Glacier Deep Archive などの耐久性のある安全な長期ストレージに直接移動できます。

#### AWS S3 関連技術
- `aws s3 sync　ｘｘｘ` については、targetはs3だよな、EFSだと、datasyncの出番になると


#### AWS ECS 関連技術
- ECR
- ECS
  - InvalidParameterException: No Container Instances were found in your cluster.
    - ネットワーク不良、必要であるパッケージがインストールされてません 
  - ECSの中、EFSをmountする
    - https://aws.amazon.com/jp/premiumsupport/knowledge-center/ecs-fargate-mount-efs-containers-tasks/
    - https://docs.aws.amazon.com/ja_jp/AmazonECS/latest/developerguide/tutorial-efs-volumes.html    
#### AWS CICD pipeline 
- [codebuild reference](https://docs.aws.amazon.com/codebuild/latest/userguide/build-spec-ref.html)
- [docker sample](https://docs.aws.amazon.com/codebuild/latest/userguide/sample-docker.html)
- 環境変数設定できる
- UnittestとECRを利用するなあｒ、artifactも必要がない


#### AWS MWAA
- dockeropertorをECSに書き換える
    - [How to work with Airflow Docker operator in Amazon MWAA](https://medium.com/@sohflp/how-to-work-with-airflow-docker-operator-in-amazon-mwaa-5c6b7ad36976) 
- MWAA CICD関連
    - CodeBuildを利用して、MWAAのCICD参考コード
        - [About Automating DAG deployment](https://github.com/aws-samples/amazon-mwaa-automating-dag-deployment)
    - [Create a CI/CD Pipeline (comprising of AWS Code* tools) for Amazon Managed Workflow for Apache Airflow (MWAA) using AWS CloudFormation.](https://github.com/aws-samples/amazon-mwaa-cicd)
    - [Deploying to Amazon Managed Workflows for Apache Airflow with CI/CD tools](https://aws.amazon.com/jp/blogs/opensource/deploying-to-amazon-managed-workflows-for-apache-airflow-with-ci-cd-tools/)

#### AWS EC2 realated
- Expand the elasic ip number
  - Find your AWS limit of elastic ip. basically 5.
  - Go to the website to apply the request for expanding the elastic ip nums.  
