<a id="top" name="top"></a>

# Amazon API Gateway Custom Authorizer Events

[<img src="/_asset/misc_home.png" alt="Back to Home" align="right">](/)
[![Go Doc][badge-doc-go]][eawsy-doc]
[![AWS Doc][badge-doc-aws]][aws-doc]

This package allows you to write an Amazon API Gateway custom authorizer that
provide control access to your API methods.

[<img src="/_asset/misc_arrow-up.png" align="right">](#top)
## Quick Hands-On

> For step by step instructions on how to author your AWS Lambda function code in Go, see
  [eawsy/aws-lambda-go-shim][eawsy-runtime].

```sh
go get -u -d github.com/eawsy/aws-lambda-go-event/...
```

```go
package main

import (
  "log"

  "github.com/eawsy/aws-lambda-go-event/service/lambda/runtime/event/apigatewayauthorizerevt"
  "github.com/eawsy/aws-lambda-go-core/service/lambda/runtime"
)

func Handle(evt *apigatewayauthorizerevt.Event, ctx *runtime.Context) (interface{}, error) {
  log.Println(evt)
  return nil, nil
}
```

[eawsy-runtime]: https://github.com/eawsy/aws-lambda-go-shim
[eawsy-doc]: https://godoc.org/github.com/eawsy/aws-lambda-go-event/service/lambda/runtime/event/apigatewayauthorizerevt

[aws-doc]: http://docs.aws.amazon.com/apigateway/latest/developerguide/welcome.html

[badge-doc-go]: http://img.shields.io/badge/api-godoc-3F51B5.svg?style=flat-square
[badge-doc-aws]: http://img.shields.io/badge/api-awsdoc-FF9800.svg?style=flat-square
