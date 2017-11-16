![SCAR](images/scar-200x200-transparent.png?raw=true)

## Introduction

### SCAR

* Is a framework to **execute containers out of Docker images in AWS Lambda**, in order to run generic applications and code in virtually any programming language on AWS Lambda.

* Is probably the easiest, most convenient approach to run applications packaged as Docker images, stored in Docker Hub, on AWS Lambda, as well as code in your favourite programming language, not only in those languages supported by AWS Lambda.

* Supports a High Throughput Computing Programming Model to create highly-parallel event-driven serverless applications that execute on customized runtime environments.

## Approach

### SCAR 

* Provides a CLI to create a Lambda function to execute a container out of a Docker image stored in Docker Hub. Each invocation of the Lambda function will result in the execution of such a container.
  * Optionally executing a shell-script inside the container for further versatility.

* Automatically defines triggers to execute the functions in response to events coming from S3 (e.g. a file upload that triggers the execution of the Lambda function to process that file).
s
## Limitations

* The Docker container must fit within the 512 MB ephemeral storage provided by AWS Lambda.
* Alpine-based Linux images cannot be currently employed.

## Use Cases

Different applications have been used in AWS Lambda via SCAR (see [examples](https://github.com/grycap/scar/tree/master/examples/) for ImageMagick, FFmpeg and AWS CLI, as well as deep learning frameworks such as Theano and Darknet) and code in virtually any programming language (see examples for R, Erlang and Elixir) on AWS Lambda.)

## License

Apache 2.0 

## Contact
Developed by the [Grid and High Performance Computing Group](https://github.com/grycap) at the [Universitat Politècnica de València](http://www.upv.es)



