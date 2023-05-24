<template>
    <div class="head-address">
        <h5>{{title}}</h5>
        <h1>{{description}}</h1>
    </div>
</template>
<script>
    export default {
    name: 'HeadAdress',
    props: {
        title: {
            type: String,
            default:() => '', 
        },
        description: {
            type: String,
            default: () => '', 
        },
    },

    }
</script>