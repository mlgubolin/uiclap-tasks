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
                &nbsp;&nbsp;
                <span>
                    Icon Placeholder:
                    <code>{{ item.icon }}</code>
                </span>
            </li>
        </ul>
    </div>
</template>