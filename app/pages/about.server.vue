<script setup lang="ts">

// this fails: why does createError not work?

throw createError({
    statusCode: 404,
    statusMessage: 'Page Not Found',
    // fatal: true,
})
</script>

<template>
    <div>
        <h1>pages / about.server.vue</h1>

        <p>
            This page should be a <a href="https://nuxt.com/docs/4.x/guide/directory-structure/app/pages#server-only-pages">server-only page</a> and throw a 404
        </p>
    </div>
</template>