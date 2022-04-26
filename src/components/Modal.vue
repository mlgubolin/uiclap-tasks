<script setup lang='ts'>
import Message from './Message.vue';
const emit = defineEmits<{
    (e: 'click', id: boolean): void
}>()

</script>

<template>
    <div class="modal">
        <div class="modal-background"></div>
        <div class="modal-content">
            <Message messageClass="message-body">
                <slot></slot>
            </Message>
        </div>
        <button class="modal-close is-large" aria-label="close" @click="emit('click', false)"></button>
    </div>
</template>
