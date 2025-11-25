Node.js → Elastic Beanstalk sample for AWS CodePipeline

Files:
- server.js
- package.json
- buildspec.yml
- .ebextensions/01_proxy.config

How it works:
1. CodePipeline: Source(GitHub: CodeStar connection) -> Build(CodeBuild) -> Deploy(Elastic Beanstalk)
2. CodeBuild runs buildspec.yml and outputs output/app.zip
3. Pipeline Deploy action (Elastic Beanstalk) deploys app.zip to your EB environment
