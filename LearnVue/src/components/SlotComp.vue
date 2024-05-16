<template>
    <h3>Component</h3>
    <div>
        <slot name="topSlot"></slot>
    </div>
    <div>
        <slot name="bottomSlot"></slot>
    </div>
</template>

<script></script>

<style scoped>
div {
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
    border-radius: 10px;
    margin: 10px;
}
</style>