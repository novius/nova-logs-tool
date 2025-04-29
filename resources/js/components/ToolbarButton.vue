<template>
    <button
        type="button"
        class="inline-flex items-center justify-center w-8 h-8 focus:outline-none focus:ring rounded-lg"
    >
        <slot />
        <Icon v-if="type" solid :name="type" />
    </button>
</template>

<script setup>
    import { Icon } from 'laravel-nova-ui';

    defineProps({
        type: {
            type: String,
            required: false,
        },
    });
</script>
