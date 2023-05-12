<template>
    <div>Hello 3</div>
    <div>{{  widget }}</div>
</template>

<script setup lang="ts">
import { DxpWidget } from "../renderer/types"
defineProps<{
    widget: DxpWidget
}>();
</script>

<style scoped>
div {
    color: red
}
</style>