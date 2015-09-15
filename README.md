rebar_protobuffs
=====

A rebar plugin for automatically compiling .proto files

Build
-----

    $ rebar3 compile

Use
---

Add the plugin to your rebar config:

    {plugins, [
        { rebar_protobuffs, ".*", {git, "git@host:user/rebar_protobuffs.git", {tag, "0.1.0"}}}
    ]}.

Then just call it directly in an existing application *before compiling*:

    $ rebar3 protobuffs compile
    ===> Fetching protobuffs
    ===> Compiling protobuffs

Alternatively, add a hook to automatically generate modules for your protobuffs:

    {provider_hooks, [
        {pre, [
            {compile, {protobuffs, compile}}
        ]}
    ]}.

Note
---
This is a work in progress and not much configuration is available at the current time. This plugin uses gpb to compile protobuffs.
