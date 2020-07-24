<template>
    <div>
        <button type="buttom" class="btn btn-danger" v-on:click="alerta()">Alerta</button>
    </div>
</template>
<script>

export default {
    name:'AlertButton',
    methods:{
        alerta(){
            alert('Alertaaaaaa!!!')
        }
    }
}
</script>