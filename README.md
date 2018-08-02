# scalaz-aws

[![Gitter](https://badges.gitter.im/scalaz/scalaz-aws.svg)](https://gitter.im/scalaz/scalaz-aws?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

# scalaz-aws

## Goal

High-performance, non-blocking and purely-functional interface to AWS APIs.

## Introduction & Highlights

Scalaz AWS is a principled functional programming library to interact with Amazon Web Services (AWS) REST APIs and (eventually) supporting all of the currently available services. Allows to create and manage infrustructure with your favourite programming language (Scala), so no need to compromise on choice of language.

* Comprehensive and consistent 
* Type safe, purely-functional
* Pluggable effect monads
* Asynchronous and non-blocking
* Streaming support
* Can be used in Scala REPLs

## Competitors

[AWS SDK 2.0](https://github.com/aws/aws-sdk-java-v2/)

| Type-safe, pure FP | Comprehensive    | Scala            |
|:------------------:|:----------------:|:----------------:|
|                  ✘ |               ✔ |         ✘ (Java) |

A rewrite of 1.0 with features like non-blocking IO and pluggable HTTP implementation. NOTE 2.0 version still a preview and is not recommended for production use yet.

[awslabs/aws-scala-sdk](https://github.com/awslabs/aws-scala-sdk)

| Type-safe, pure FP | Comprehensive    | Scala            |
|:------------------:|:----------------:|:----------------:|
|                  ✘ |               ✘ |                ✔ |

Uses generators to wrap Java code into Scala. Motto `It's like the AWS SDK for Java, but more Scala-y`

[Scala wrapper for AWS SDK](https://bitbucket.org/atlassian/aws-scala)

| Type-safe, pure FP | Comprehensive    | Scala            |
|:------------------:|:----------------:|:----------------:|
|                  ✘ |               ✘ |                ✔ |

Backed up by Attlassian. Though, the library seems to be abandoned (or not actively maintained). It looks like they experimented with `akka` and `scalaz-streams`, though there is no documentation on it.

[AWScala: AWS SDK on the Scala REPL](https://github.com/seratch/AWScala)

| Type-safe, pure FP | Comprehensive    | Scala            |
|:------------------:|:----------------:|:----------------:|
|                  ✘ |               ✘ |                ✔ |

Motto `Using AWS SDK on the Scala REPL`. AWScala enables Scala developers to easily work with Amazon Web Services in the Scala way. Though AWScala objects basically extend AWS SDK for Java APIs, you can use them with less stress on Scala REPL or sbt console.

[alpaka/based on Akka streams](https://developer.lightbend.com/docs/alpakka/current/)

| Type-safe | Pure FP | Comprehensive | Scala            |
|:---------:|:-------:|:-------------:|:----------------:|
|        ✔ |       ✘ |             ✔ |               ✔ |

Provides a number of connectors for streaming data in and out using Akka streams.

[streamz/fs2 wrapper on camel](https://github.com/krasserm/streamz/tree/master/streamz-camel-fs2)

| Type-safe | Pure FP | Comprehensive | Scala            |
|:---------:|:-------:|:-------------:|:----------------:|
|        ✔ |       ✔ |             ✔ |               ✔ |

This is a fs2 wrapper for camel which isolates effects and providing a possibly pure FP library. Big advantage is that one can use any camel component to receive or push data to.

[Scala client for Amazon S3](https://github.com/bizreach/aws-s3-scala)

| Type-safe, pure FP | Comprehensive    | Scala            |
|:------------------:|:----------------:|:----------------:|
|                  ✘ |               ✘ |                ✔ |

S3 only. Provides mock implementation which works on the local file system.

[Asynchronous Scala Clients for AWS](https://github.com/dwhjames/aws-wrap)

| Type-safe, pure FP | Comprehensive    | Scala            |
|:------------------:|:----------------:|:----------------:|
|                  ✘ |               ✘ | ✔ (2.10.x, 2.11.x) |

Abandonned from 2015. Scala versions 2.10.x and 2.11.x and AWS Java SDK 1.10.x.

## Alternatives

[Amazon Web Services SDK for Haskell](https://github.com/brendanhay/amazonka)

| Type-safe, pure FP | Comprehensive    | Scala            |
|:------------------:|:----------------:|:----------------:|
|                  ✔ |               ✔ |       ✘ (Haskell)|


[Amazon Web Services for Haskell](https://github.com/aristidb/aws)

| Type-safe, pure FP | Comprehensive    | Scala            |
|:------------------:|:----------------:|:----------------:|
|                  ✔ |               ✘ |       ✘ (Haskell)|

## Background

[Amazonka - motivation and design decisions](http://brendanhay.nz/amazonka-comprehensive-haskell-aws-client)

[Optimizing Tagless Final – Saying farewell to Free](https://typelevel.org/blog/2017/12/27/optimizing-final-tagless.html)

[Tagless Final algebras and Streaming](https://typelevel.org/blog/2018/05/09/tagless-final-streaming.html)

[Amazon S3 REST API Introduction](https://docs.aws.amazon.com/AmazonS3/latest/API/Welcome.html)
