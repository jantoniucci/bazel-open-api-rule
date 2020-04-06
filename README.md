# bazel opeanapi v3 rule

##### Motivations

There are many other rules for [openapi](https://www.openapis.org/) code generation like:
* [openapi-generator-bazel](https://github.com/OpenAPITools/openapi-generator-bazel)
* [meetup/rules_openapi](https://github.com/meetup/rules_openapi)
* [openapi-generator](https://github.com/OpenAPITools/openapi-generator)

I found they are:
* Not supporting Bazel 2.2
* Not supporting openapi-generator-ignore
* Abandoned (last updates > 6 months)

So I decided to create this one based on those previous:
```sh
git clone https://github.com/jantoniucci/bazel-open-api-rule.git
```

## Run it!
```sh
bazel build //sample/api:api-server
```