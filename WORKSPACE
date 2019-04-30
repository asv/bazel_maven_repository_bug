load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

MAVEN_REPOSITORY_RULES_VERSION = "1.0"
MAVEN_REPOSITORY_RULES_SHA = "5950eb0e4a3b8fd39832e58dd30e96258526751dabdc308cc7216f74396d8d41"

http_archive(
    name = "maven_repository_rules",
    sha256 = MAVEN_REPOSITORY_RULES_SHA,
    strip_prefix = "bazel_maven_repository-%s" % MAVEN_REPOSITORY_RULES_VERSION,
    urls = ["https://github.com/square/bazel_maven_repository/archive/%s.zip" % MAVEN_REPOSITORY_RULES_VERSION],
)

load("@maven_repository_rules//maven:maven.bzl", "maven_repository_specification")
maven_repository_specification(
    name = "maven",
    artifacts = {
        "com.google.guava:guava:26.0-jre": { "insecure": True },
        "com.google.code.findbugs:jsr305:3.0.2": { "insecure": True },
        "org.checkerframework:checker-qual:2.5.2": { "insecure": True },
        "com.google.errorprone:error_prone_annotations:2.1.3": { "insecure": True },
        "com.google.j2objc:j2objc-annotations:1.1": { "insecure": True },
        "org.codehaus.mojo:animal-sniffer-annotations:1.14": { "insecure": True },
    },
)

JAVA_GRPC_REPOSITORY_RULES_VERSION = "1.20.0"
JAVA_GRPC_REPOSITORY_RULES_SHA = "553d1bdbde3ff4035747c184486bae2f084c75c3c4cdf5ef31a6aa48bdccaf9b"

http_archive(
    name = "io_grpc_grpc_java",
    sha256 = JAVA_GRPC_REPOSITORY_RULES_SHA,
    strip_prefix = "grpc-java-%s" % JAVA_GRPC_REPOSITORY_RULES_VERSION,
    urls = ["https://github.com/grpc/grpc-java/archive/v%s.tar.gz" % JAVA_GRPC_REPOSITORY_RULES_VERSION],
)

load("@io_grpc_grpc_java//:repositories.bzl", "grpc_java_repositories")
grpc_java_repositories()
