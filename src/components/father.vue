<template>
    <div>

        <p>我是父组件,fromSon的值是：{{fromSon}}</p>
        <div class="son-css">
            <Son :toSon="toSon" @toFather="toFather" />
        </div>

    </div>
</template>

<script>
import Son from "./son";
export default {
    name: 'father',
    components: { Son },
    data () {
        return {
            toSon: '儿子，你好啊',
            fromSon: '4'
        }
    },
    mounted () {

    },
    methods: {
        toFather (msg) {
            this.fromSon = msg;

        }
    }

}
</script>

<style>
.son-css {
    width: 200px;
    height: 200px;
    background: #ccc;
}
</style>