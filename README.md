![SCAR](images/scar-200x200-transparent.png?raw=true)

## Introduction

### SCAR

* Is a framework to execute containers out of Docker images in AWS Lambda, in order to run generic applications and code in virtually any programming language on AWS Lambda.

* Is probably the easiest, most convenient approach to run applications packaged as Docker images, stored in Docker Hub, on AWS Lambda, as well as code in your favourite programming language, not only in those languages supported by AWS Lambda.

## Approach

### SCAR 

* Provides a CLI to create a Lambda function to execute a container out of a Docker image stored in Docker Hub. Each invocation of the Lambda function will result in the execution of such a container.
  * Optionally executing a shell-script inside the container for further versatility.

* Automatically defines triggers to execute the functions in response to events coming from S3 (e.g. a file upload that triggers the execution of the Lambda function to process that file).

### SCAR in a nutshell

Create a Lambda function to execute a container out of the [ubuntu:16.04](https://hub.docker.com/r/library/ubuntu/tags/16.04/) Docker image in Docker Hub.

```sh
scar init ubuntu:16.04
```

Execute a command (or a shell-script) inside the container running on AWS Lambda:

```sh
scar run scar-ubuntu-16-04 whoami
sbx_user1061
```

That is the basics, but SCAR goes way beyond. It supports a High Throughput Computing Programming Model to create highly-parallel event-driven serverless applications that execute on customized runtime environments. See the [documentation](https://github.com/grycap/scar).

### Limitations

* The Docker container must fit within the 512 MB ephemeral storage provided by AWS Lambda.
* Alpine-based Linux images cannot be currently employed.

## Use Cases

Different applications have been used in AWS Lambda via SCAR (see [examples](https://github.com/grycap/scar/tree/master/examples/README.md) for ImageMagick, FFmpeg and AWS CLI, as well as deep learning frameworks such as Theano and Darknet) and code in virtually any programming language (see examples for R, Erlang and Elixir) on AWS Lambda.

It can be considered the way-to-go tool for serverless scientific computing.

## License

Apache 2.0 

## Contact
Developed by the [Grid and High Performance Computing Group](https://github.com/grycap) at the [Universitat Politècnica de València](http://www.upv.es).



