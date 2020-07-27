<template>
  <div id="app">
    <div class="container mt-5">
      <div class="row">
        <div class="col-sm-3">
          <AlertButton /> <br> <MessageButton message="Oi Imundo!!!!" titleButton="Oi" />
          <br> <MessageButton message="Hello Kit" titleButton="Hello"/>
          <br> <TextButton titleButton="Insere"  message="EStou escrevendo um texto" @texto="escrever"  />
        </div>
      </div>
      <div class="row">
        <div class="col-sm-3">
          <strong>{{meuTexto.text}}</strong>
        </div>
      </div>
      
        <CustomList />     
        <ViewPass label="Senha" />    
        
         <ListFruits />
        
      </div>
       
      
      
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css';
import 'font-awesome/css/font-awesome.css';


import AlertButton from './components/AlertButton';
import MessageButton from './components/MessageButton';
import TextButton from './components/TextButton';
import CustomList from './components/CustomList';
import ViewPass from './components/ViewPass';
import ListFruits from './components/ListFruits';
export default {
  name: 'App',
  components: {
    AlertButton,MessageButton,TextButton,CustomList,ViewPass,ListFruits
  },
  data:()=>{
    return{
      meuTexto:''
    }
  },
  methods:{
    escrever(load){
      this.meuTexto=load
    }
  }

}
</script>

