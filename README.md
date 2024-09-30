Cloudflare Bindings to API
======

Cloudflare provides a lot of good, and cheap services, like KV, D1, etc.
But they are not so easy to use, developers have to read the documents,
deploy services, and change their codes.

Because Cloudflare use Edge Runtime as their serverless platform, 
integration the bindings to your existing code might bring you a lot of
troubles. I think maybe, access your Cloudflare services from HTTP API
is a good idea.

So I build this repo to make this work easier. For example, you want to
build a product, and you need the KV service, you can fork this repo, 
deploy the `/pacages/kv` folder as a worker to your cloudflare account,
then you can access your KV service from HTTP API.

For detailed configuration, you can check the README.md in each folder.


Why not official HTTP API?
--------

1. There are very few options to control permission when using the official API.
2. The official API is not compatible with other SDK, like Upstash,
    developers may need to build more code to work with every servies.


Available Services
--------

- [Redis -> KV](./packages/kv/README.md)
