<template>
    <div>
        <h1>{{ item.title }}</h1>
        <p><b>Ingredients:</b> {{ item.ingredients }}</p>
        <img :src="item.thumbnail" height="300"/>
    </div>
</template>

<script>
export default {
    name: 'RecepieItem',
    props: {
       item: Object 
    }
}
</script>