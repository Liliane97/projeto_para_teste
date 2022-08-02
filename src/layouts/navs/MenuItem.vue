<script setup lang="ts">
    import { defineProps } from 'vue';
    // definindo uma props para usar os icones no itens do menu de forma dinâmica
    defineProps({
        icon:{default:null}
    });
</script>

<template>
    <div class="flex items-center space-x-4">
        <div class="bg-orange-500 p-2 rounded-lg">
            <!-- definindo  componente dinâmico -->
            <component :is="icon" class="w-4 h-4"/>
        </div>
        <span>
            <slot></slot>
        </span>
    </div>
</template>