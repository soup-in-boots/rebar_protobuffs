rebar_protobuffs
=====

A rebar plugin

Build
-----

    $ rebar3 compile

Use
---

Add the plugin to your rebar config:

    {plugins, [
        { rebar_protobuffs, ".*", {git, "git@host:user/rebar_protobuffs.git", {tag, "0.1.0"}}}
    ]}.

Then just call it directly in an existing application:

    $ rebar3 protobuffs compile
    ===> Fetching protobuffs
    ===> Compiling protobuffs
