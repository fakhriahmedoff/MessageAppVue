<template>
            
            <a-button v-if="loading == true" type="primary" size="big" >Sending {{count}}</a-button>
            <a-button v-els type="primary" size="big" >Send {{count}}</a-button>

</template>

<script>
export default {
    name: 'MyBtn',
    props: ['count', 'loading'],
}
</script>

<style>

</style>