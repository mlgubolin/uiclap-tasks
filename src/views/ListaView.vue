<script setup lang="ts">
import jsonFile from "../assets/lista.json"
import type { ItemIcon } from "@/types/ItensIcon";

const items: Array<ItemIcon> = JSON.parse(JSON.stringify(jsonFile))
console.log(items)
</script>

<template>
    <div class="content">
        <ul>
            <li v-for="item in items" :key="item.value">
                {{ item.label }}
                <i :class="item.icon"></i>
            </li>
        </ul>
    </div>
</template>