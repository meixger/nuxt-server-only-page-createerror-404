<script setup lang="ts">
</script>

<template>
    <div>
        <h1>pages / index.vue</h1>

        <p>
            Description: Nuxt
            <a href="https://nuxt.com/docs/4.x/guide/directory-structure/app/pages#server-only-pages" target="_blank">
                server-only pages⤴</a>
            should support <code>throw createError({ statusCode: 404})</code>.
        </p>
        <p>
            Expected: By navigating to <a href="/about">/about</a> a <code>404 Not Found</code> should be returned.
        </p>
        <p>
            Actual: A <code>200 OK</code> is returned.
        </p>

        <hr />

        <div style="display: flex; flex-direction: column; gap: 1rem;">

            <div>
                <a href="/about">/about</a>
                -
                <code>app/pages/about.server.vue</code>
                -
                <b>Fails, <code>throw createError()</code> within a server-only page seems to fail returning a <code>404 Not Found</code>.</b>
            </div>

            <div>
                <a href="/contact">/contact</a>
                -
                <code>app/pages/contact.vue</code>
                - works as intended, a <code>404 Not Found</code> is returned
            </div>

            <div>
                <a href="/page-that-does-not-exist">/page-that-does-not-exist</a>
                -
                works as intended, page doesn't exist and a <code>404 Not Found</code> is returned
            </div>
        </div>
    </div>
</template>