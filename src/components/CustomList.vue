<template>
    <div class="row">
        
            <div class="col-sm-3">
                <div class="form-group">
                    <label for="esquerda">Esquerda</label>
                    <select  :multiple="true" class="form-control " id="esquerda" v-model="modelo.direita" >
                        <option v-for="(esq,index) in esquerda" :key="index" :value="index" >{{esq}}</option>
                    </select>
                    
                </div>
            </div>
                <div class="col-sm-3 mt-5">
                    <button type="button" class="btn btn-outline-info " @click="enviarEsquerda()" ><span class="fa fa-chevron-left" aria-hidden="true"></span></button>
                    <button type="button" class="btn btn-outline-info " @click="enviarDireita()"><span class="fa fa-chevron-right" aria-hidden="true"></span></button>
                </div>
            <div class="col-sm-3">
                <div class="form-group">
                    <label for="direita">Direita</label>
                    <select :multiple="true" class="form-control " id="direita"  v-model="modelo.esquerda" >
                        <option v-for="(dir,index) in direita" :key="index" :value="index" >{{dir}}</option>
                    </select>
                    
                </div>
            </div>   
    </div>
</template>
<script>
export default {
    name:'CustomList',
    data:()=>{
        return{
            esquerda:['Banana','Melão','Maçã','Abacaxi'],
            direita:[],
            modelo:{
                esquerda:[],
                direita:[]
            }
        }
    },
    methods:{
        enviarDireita(){
                const index=this.modelo.direita[0];
            this.direita.push(this.esquerda[index]);
            //this.esquerda.indexOf(index,1);
            
            this.$delete(this.esquerda,index);
            //this.esquerda.slice(index,1); 

        },
        enviarEsquerda(){
                const index=this.modelo.esquerda[0];
            this.esquerda.push(this.direita[index]);
            //this.esquerda.indexOf(index,1);

            this.$delete(this.direita,index);
            //this.esquerda.slice(index,1); 

        }
    }
    
}
</script>
<style >    
    .aumentar{
        width: 10em;
    }

</style>