<template>
    <div class="container">
            <div class="header-style">
                <header-top></header-top>
            </div>
            <div class="my-wrapper">
                <div>
                    <h3>Rentrez Vos Choses A faire</h3>
                    <form class="formulaire">
                        <label for="task">Action</label>
                        <input v-model="formData.task" type="text" id="task" class="form-control">
                        <button class="btn btn-primary" v-on:click.prevent="addData">crée une tache</button>
                    </form>
                </div>
                <div class="liste-style">
                    <ul>
                        <li v-bind:key="index" v-for="(task, index) in myAllTasks">
                            <liste v-bind:id="index" :task="task" :suppression="suppression"></liste>
                        </li>
                    </ul>
                       
                </div>
            </div>
    </div>
</template>
<script>
import Header from "./content_components/Header.vue"
import Liste from "./content_components/Liste.vue"
    export default {
    name: 'Contains',
    components: {
        'header-top': Header,
        'liste': Liste,
    },
    data() {
        return {
            myAllTasks: ['React', 'Javascript', 'Node Js', 'Tailwind Css', 'Style Css' ],
            infoSubmit: false,
            formData:{
                task:''
            }
        }
    },
    methods: {
            addData: function(){
            this.myAllTasks.push(this.formData.task)
            this.formData.task = ''
            },
            suppression: function(e) {
                this.myAllTasks.splice(e.target.parentNode.id, 1)
            }
    
    }
    }
</script>
<style scoped>
body{
    margin: 0;
    padding: 0;
    width: 100%;
    height: auto;
}
.liste-style{
    margin-top :20px;

}
.my-wrapper{    
    display: flex;
    flex-direction: column;
    
}
.my-wrapper > h3{
    padding-top: 10px;
}

.container{
    width: 100%;
    height: auto;
    margin-top: 50px;
}
.formulaire{
    display: flex;
    flex-direction: column;
}
.formulaire > label{
    margin-bottom: 10px;
    color: rgba(0, 0, 0, 0.5);
}
button{
    margin-top: 10px;
    width: 150px;
}
ul{
    list-style: none;
    
}
li{
    padding-bottom: 3px;
}
</style>