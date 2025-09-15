<script setup lang="ts">

// this works as intended

throw createError({
    statusCode: 404,
    statusMessage: 'Page Not Found',
    fatal: true,
})
</script>

<template>
    <div>
        <h1>pages / contact.vue</h1>

        <p>
            This page should throw a 404
        </p>
    </div>
</template>