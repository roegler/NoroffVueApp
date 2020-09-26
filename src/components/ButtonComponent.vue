<template>
    <button class="primary-btn" v-text="title"></button>
</template>

<script>
export default {
    props: {
        title: String
    }
};
</script>

<style>
.primary-btn {
    background: blue;
    color: cornsilk;
    border: none;
}
</style>
    