<template>
    <div>
        <ul class="list-group" v-for="(f,index) in frutas" :key="index">
            <li class="list-group-item" >
                <span class="float-left">{{f}}</span>
                <span class="float-right">
                    <button type="button" class="btn btn-outline-info tamanho"  @click="del(index)">
                        <span class="fa fa-trash"></span>
                    </button>
                </span>
            </li>
        </ul>
        <div class="input-group mt-5 mb-5">
           
            <input type="text" class="form-control" id="campo" v-model="container" aria-label="Frutas"  aria-describedby="plus">
                <div class="input-group-append" id="plus">
                    <button  type="button" class="btn btn-outline-info" @click="plus()">
                        <span class="fa fa-plus"></span>
                    </button> 
                </div>
        </div>
    </div>
</template>
<script>
export default {
    name:'ListFruits',
    data:()=>{
        return{
            frutas:['mamão','banana','pera'],
            container:[],
            element:''
        }
    },
    methods:{
        del(val){
            const index=val;
            this.$delete(this.frutas,index);
        },
        plus(){
            const total=this.frutas.length;

            this.$set(this.frutas,total,this.container)
            
        },
        
    },
    
}
</script>
<style >
    .tamanho{
        width:2em;
        height: auto;
    }
</style>