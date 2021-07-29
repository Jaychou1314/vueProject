<template>
    <div>
        我是子组件
        {{toSon}}
        <button @click="handleClick()">点击传给父组件</button>
    </div>
</template>

<script>
export default {
    name: 'son',
    props: {
        toSon: {
            type: String,
            default: ''
        }
    },
    data () {
        return {

        }
    },
    methods: {
        handleClick () {
            this.$emit('toFather', '我是儿子')
        }
    }
}
</script>

<style scoped>
</style>
