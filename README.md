# Nuxt server-only components and 404 NotFound

Nuxt [server-only pages⤴](https://nuxt.com/docs/4.x/guide/directory-structure/app/pages#server-only-pages)
should support `throw createError({ statusCode: 404})`.

The server-only page [/app/pages/about.server.vue](/app/pages/about.server.vue) should return a `404 NotFound` by `throw createError({ statusCode: 404})`.