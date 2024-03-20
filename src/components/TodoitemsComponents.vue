<template>
    <div class="todoitems">
        <div class="check">
            <input type="checkbox" @change="isChecked" @click="!isChecked" id="ischecked">
            <label for="ischecked" :class="!isChecked? '' :'notchecked'">{{ name }} </label>
            
        </div>
        <img src="../assets/trash_30px.png" width="20" height="20" >
    </div>
  </template>
  
  <script>
  
  export default {
    name: 'TodoitemsComponents',
    components: {
    
    },
    props:[
        'name',
        'isChecked',
        'delete',
        ]
    
  }
  </script>
  
  <style> 
  .todoitems{
    width: 100%;
    height: 50px;
    display: inline-flex;
    justify-content: space-between;
    border-bottom: 2px solid #404040;
  }
  .check{
    display: inline-flex;
  }
  label{
    padding-top: 15px;
  }
img{
    padding-top: 15px;
    margin-right: 15px;
}
input{
    margin-top: 8px;
    
}
.notchecked{
  text-decoration: overline;
}
  

  </style>
  