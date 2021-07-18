<template>
    <div>
        <div>
            <h3>{{ message }}</h3>
        </div>
        <div>
            <button @click.prevent="emitToParent">From Child</button>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        message: String
    },
 
    methods:{
        emitToParent() {//passing data to parent from child
            this.$emit('childToParent', "To parent from child")
        }
    }
}
</script>