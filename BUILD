load("//configure_make:def.bzl", "cc_configure_make")

cc_configure_make(
    name = "libevent",
    src = "@libevent//:all",
    configure_flags = [
        "--enable-shared=no",
        "--disable-libevent-regress",
        "--disable-openssl",
    ],
    out_lib_path = "lib/libevent.a",
)

cc_binary(
    name = "libevent_echosrv1",
    srcs = ["libevent_echosrv1.c"],
    deps = [
        "libevent",
    ],
)

cc_configure_make(
    name = "cares",
    src = "@cares//:all",
    configure_flags = [
        "--enable-shared=no",
        "--enable-lib-only",
        "--enable-debug",
        "--enable-optimize",
    ],
    out_lib_path = "lib/libcares.a",
)

cc_binary(
    name = "async_dns",
    srcs = ["async_dns.c"],
    deps = [":cares"],
)
