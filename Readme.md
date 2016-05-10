EC2-S3-Download
===

About
==

A simple tool to download objects from S3 on EC2 instances. It was written to retrieve private files via IAM rules for instances when bootstrapping machines. Written in go it can be used as an easily deployable alternative to other tools on reduced environments like CoreOS.

Usage
==

```
./ec2-s3-download
  -bucket string
    	s3 bucket
  -dest-path string
    	destination path (optional)
  -file-path string
    	object path (w/o bucket)
  -region string
    	s3 bucket
```

Build
==

Go 1.5+ on OSX targetting linux:

```
go get -u github.com/aws/aws-sdk-go
GOOS=linux go build ec2-s3-download.go
```
