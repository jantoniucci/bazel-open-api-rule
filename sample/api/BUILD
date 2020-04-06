load("//bazel-rules/openapi:openapi.bzl", "openapi_gen")

openapi_gen(
  name = "api-server-src",
  language = "spring",
  spec = "rest-api.yaml",
  system_properties = {
    "apiTests": "true",
    "modelTests": "true",
  },
  additional_properties = {
    "java8": "true",
  },
  ignoreFile = ".openapi-generator-ignore",  
  api_package = "virtualBank.savingsAccountServer.api",
  model_package = "virtualBank.savingsAccountServer.model",
  invoker_package = "virtualBank.savingsAccountServer",
)

java_library(
  name = "api-server",
  srcs = [":api-server-src"],
  visibility = ["//visibility:public"],
  deps = [
    "@maven//:com_fasterxml_jackson_core_jackson_annotations",
    "@maven//:com_fasterxml_jackson_core_jackson_databind",
    "@maven//:io_springfox_springfox_core",
    "@maven//:io_springfox_springfox_spi",
    "@maven//:io_springfox_springfox_spring_web",
    "@maven//:io_springfox_springfox_swagger2",
    "@maven//:io_springfox_springfox_swagger_ui",
    "@maven//:io_swagger_swagger_annotations",
    "@maven//:javax_validation_validation_api",
    "@maven//:javax_xml_bind_jaxb_api",
    "@maven//:org_apache_tomcat_embed_tomcat_embed_core",
    "@maven//:org_apache_tomcat_tomcat_annotations_api",
    "@maven//:org_openapitools_jackson_databind_nullable",
    "@maven//:org_springframework_boot_spring_boot",
    "@maven//:org_springframework_boot_spring_boot_autoconfigure",
    "@maven//:org_springframework_boot_spring_boot_starter_web",
    "@maven//:org_springframework_spring_beans",
    "@maven//:org_springframework_spring_context",
    "@maven//:org_springframework_spring_web",
    "@maven//:org_springframework_spring_webmvc",
  ],
)