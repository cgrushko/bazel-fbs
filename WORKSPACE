new_http_archive(
    name = "libevent",
    build_file_content = """filegroup(name = "all", srcs = glob(["**"]), visibility = ["//visibility:public"])""",
    strip_prefix = "libevent-2.1.8-stable",
    urls = ["https://github.com/libevent/libevent/releases/download/release-2.1.8-stable/libevent-2.1.8-stable.tar.gz"],
)

new_http_archive(
    name = "cares",
    build_file_content = """filegroup(name = "all", srcs = glob(["**"]), visibility = ["//visibility:public"])""",
    strip_prefix = "c-ares-1.14.0",
    urls = ["https://c-ares.haxx.se/download/c-ares-1.14.0.tar.gz"],
)
