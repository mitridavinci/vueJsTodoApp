<template>
        
             <div class="card" >
                <div class="btn-supr btn-danger btn"  v-on:click="suppression">X</div>
                  <div class="card-body">
                            {{task}}
                  </div>
                  
            </div>   
        
</template>
<script>
export default {
    name: 'Liste',
    props: ['task', 'suppression'],
    
    }
</script>
<style scoped>


 .btn-supr{
    position: absolute;
    top: 1px;
    right: 1px;
    z-index: 1;
 }

.btn-supr.btn{
    cursor: pointer;
}
 .card{
    position: relative;
    width: 800px;
    height: 50px; 
 }

</style>