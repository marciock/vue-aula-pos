<template>
    <div>
        <button type="buttom" class="btn btn-warning" v-on:click="insere()">{{titleButton}}</button>
    </div>
</template>
<script>

export default {
    name:'AlertButton',
    props:['message','titleButton'],
    methods:{
        insere(){
           // this.$emit('texto',{text:'texto escrito'})
            this.$emit('texto',{text:this.message})
        }
    }
}
</script>