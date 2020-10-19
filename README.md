## Boilerplate for npm project with s3 deploy

### Setup
1. Connect github repo with Travis
2. Create neccessary env vars in Travis project allowing deploys to AWS S3
```
docker run -it -v $(pwd):/project --rm --entrypoint=/bin/sh traviscli
/project # travis login --github-token TOKEN
/project # travis env set AWS_ACCESS_KEY_ID <access key> --repo oversizedhat/s3deploy
/project # travis env set AWS_SECRET_ACCESS_KEY <secret access key> --repo oversizedhat/s3deploy
```
3. Make sure deploy info is correct in .travis.yml (bucket name, region etc)