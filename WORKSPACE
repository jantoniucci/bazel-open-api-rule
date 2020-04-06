load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

RULES_JVM_EXTERNAL_TAG = "3.0"
RULES_JVM_EXTERNAL_SHA = "62133c125bf4109dfd9d2af64830208356ce4ef8b165a6ef15bbff7460b35c3a"

http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    sha256 = RULES_JVM_EXTERNAL_SHA,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

http_archive(
    name = "bazel_common",
    strip_prefix = "bazel-common-f1115e0f777f08c3cdb115526c4e663005bec69b",
    url = "https://github.com/google/bazel-common/archive/f1115e0f777f08c3cdb115526c4e663005bec69b.zip",
)

load("//bazel-rules/openapi:openapi.bzl", "openapi_repositories")
openapi_repositories()

load("@rules_jvm_external//:defs.bzl", "maven_install")
maven_install(
    artifacts = [
        "org.hamcrest:hamcrest-library:1.3",
        "org.springframework.boot:spring-boot-autoconfigure:2.1.3.RELEASE",
        "org.springframework.boot:spring-boot-test-autoconfigure:2.1.3.RELEASE",
        "org.springframework.boot:spring-boot-test:2.1.3.RELEASE",
        "org.springframework.boot:spring-boot:2.1.3.RELEASE",
        "org.springframework.boot:spring-boot-starter-web:2.1.3.RELEASE",
        "org.springframework:spring-beans:5.1.5.RELEASE",
        "org.springframework:spring-context:5.1.5.RELEASE",
        "org.springframework:spring-test:5.1.5.RELEASE",
        "org.springframework:spring-web:5.1.5.RELEASE",
        "io.springfox:springfox-swagger2:2.8.0",
        "io.springfox:springfox-swagger-ui:2.8.0",
        "javax.xml.bind:jaxb-api:2.2.11",
        "org.openapitools:jackson-databind-nullable:0.1.0",
        "io.swagger:swagger-annotations:1.5.22",
        "com.google.code.findbugs:jsr305:3.0.2",
        "com.squareup.okhttp3:okhttp:3.14.2",
        "com.squareup.okhttp3:logging-interceptor:3.14.2",
        "com.google.code.gson:gson:2.8.5",
        "io.gsonfire:gson-fire:1.8.3",
        "org.apache.commons:commons-lang3:3.9",
        "junit:junit:jar:4.13"
    ],
    fetch_sources = True,
    maven_install_json = "//:maven_install.json",
    repositories = [
        "https://jcenter.bintray.com",
    ],
)

load("@maven//:defs.bzl", "pinned_maven_install")
pinned_maven_install()
