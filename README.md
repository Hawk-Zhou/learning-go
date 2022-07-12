# Learning-Go

## Intro
This repo contains code I wrote/modified based on others' code that is valuable to me.

## Concurrency  
- concur_putting_everything_together.go

  > This is based on the example *Putting Our Concurrent Tools Together* from *Learning Go: An Idiomatic Approach to Real-World Go Programming*, Ch 10.
  >
  > The OG code excerpt is not runnable because there is no actually implementation of sending request. I implemented a timer that ticks every 50ms and a fake request interface that imitate the process of requesting something over Internet and gives predetermined results (success, failure, timeout) for testing purpose.
  
  The code simulates an situation where the program have to send request `siteA` and `siteB` to get responses. The responses from `siteA` and `siteB` are used as input to request `siteC`. We see that requesting `siteA` and `siteB` can be done concurrently. It's assumed that for any request, there are three possible outcomes, success, fail and timeout (which takes `100ms` to be detected). Moreover, `50ms` is allowed for the whole process.
