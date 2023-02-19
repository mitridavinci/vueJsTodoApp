<template>
        <header>
           <h2>{{ titre }}</h2> 
        </header>

</template>
<script>
      export default {
            name: 'Header',
            data(){
                return{
                    titre: 'Notre To Do List'
                }
            }
    }
</script>
<style scoped>

    header{
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            background: #000;
            color: #f1f1f1;
            padding: 10px;
            text-align: center;
            font-size: 2em;
            font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
            overflow-x: hidden;
            margin: 0;
    }
</style>