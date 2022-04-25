<template>
    <div class="modal">
        <div class="modal-background"></div>
        <div class="modal-content">
            <div class="message is-info">
                <div class="message-body">
                    <slot></slot>
                </div>
            </div>
        </div>
        <button class="modal-close is-large" aria-label="close" @click="$emit('fechaModal', false)"></button>
    </div>
</template>

<script lang='ts'>
export default {
    name: 'Modal',
}
</script>