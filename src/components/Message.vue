<script setup lang="ts">
const props = defineProps<{
    messageClass: string
}>();
</script>

<template>
    <div class="message is-info">
        <div :class="props.messageClass">
            <slot></slot>
        </div>
    </div>
</template>
