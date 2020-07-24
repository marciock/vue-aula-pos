<template>

    <div class="form-group ">
        <label for="password">{{label}}</label>
        <div class="input-group">
            <input type="password" class="form-control" id="password" v-model="senha" v-if="view===false" aria-describedby="buttons">
            <input type="text" class="form-control" id="password" v-model="senha"  v-if="view===true" aria-describedby="buttons">
            <div class="input-group-append" id="buttons">
                <button type="button" class="btn btn-outline-info" @click="showPass()">
                    <span class="fa fa-eye"></span>
                </button>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name:'ViewPass',
    props:['label'],
    data:()=>{
        return{
            senha:'',
            view:false
        }
        
    },
    methods:{
        showPass(){
            if(this.view===false){
                this.view=true;
                console.log(this.view);
            }else{
                this.view=false;
                console.log(this.view);
            }
        }
    }

}
</script>