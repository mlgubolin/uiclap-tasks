<script setup lang="ts">
import Botao from '@/components/Botao.vue';
import { ref } from 'vue';
import Modal from '../components/Modal.vue';

const mostraModal = ref(false);

</script>

<template>
    Sobre:
    <Botao label="Info" class="is-info" @click="mostraModal = true"></Botao>
    <Modal
        :class="{ 'is-active': mostraModal }"
        @click="(setModal: boolean) => mostraModal = setModal"
    >Algumas informações sobre o app??</Modal>
</template>