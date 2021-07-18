<template>
    <Child message="hellooo from parent" @childToParent="onChildClick"/>
</template>

<script>

import Child from './Child.vue'

export default {
    components: {
        Child
    },
    methods:{
        onChildClick(value) {
            alert(value);
        }
    }
}

</script>
