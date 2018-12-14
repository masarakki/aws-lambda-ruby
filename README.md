# aws-lambda-ruby

Ruby docker image for building sam package.

```sh
#!/bin/sh

docker run -it -v `pwd`:`pwd` -u `id -u`:`id -g` -w `pwd` masarakki/aws-lambda-ruby bundle install --deployment
sam package --template-file template.yaml --output-template-file packaged-template.yaml --s3-bucket {YOUR_BUCKET_NAME}
sam deploy --template-file packaged-template.yaml --stack-name {YOUR_STACK_NAME} --capabilities CAPABILITY_IAM
rm -r .bundle

```

## License

CC0

DEAR AWS, PLEASE SUPPORT OFFICIAL IMAGE LIKE THIS !!!!
