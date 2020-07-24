<template>
    <div>
        <button type="buttom" class="btn btn-success" v-on:click="alerta()">{{titleButton}}</button>
    </div>
</template>
<script>

export default {
    name:'AlertButton',
    props:['message','titleButton'],
    methods:{
        alerta(){
            const mes=this.message
            alert(mes)
        }
    }
}
</script>