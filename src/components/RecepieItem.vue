<template>
    <div>
        <h1>{{ item.title }}</h1>
        <ButtonComponent :title="'Read more'"/>
        <p><b>Ingredients:</b> {{ item.ingredients }}</p>
        <img :src="item.thumbnail" height="300"/>
    </div>
</template>

<script>
import ButtonComponent from "./ButtonComponent.vue"

export default {
    name: 'RecepieItem', 
    components: {
        ButtonComponent
    },
    props: {
       item: Object 
    }
}
</script>