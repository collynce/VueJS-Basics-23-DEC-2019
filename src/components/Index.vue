<template>
    <div>
        <div>
            <ul v-for="todos in todo" :key="todos.id">
                <li>{{todos.name}}</li>
            </ul>
            <button @click="triggerAlert">Show Date</button>
        </div>
        <div>
            <form>
                <input type="text" placeholder="Enter Name" v-model="formDatas.myname"/>
                <span>{{formDatas.myname}}</span>
                <br>
                <input type="text" placeholder="Enter Password" v-model="formDatas.passWord"/>
                <span>{{formDatas.passWord}}</span>

            </form>
            <button @click="clearData">Clear</button>
        </div>
    </div>
</template>
<script>
    export default {
        name: 'Index',
        data() {
            return {
                isDisabled: true,
                myname:'',
                passWord: '',
                todo: {
                  todo1:{
                      id: 1,
                      name: 'Task One',
                  },
                    todo2:{
                      id: 2,
                      name: 'My Name',
                  },
                },
                formDatas:{}
            }
        },
        methods: {
            triggerAlert(){
                const today = new Date();
                const todays = today.getDate() + '/' + today.getMonth() + '/' + today.getFullYear() ;
                alert('Today is' + '  ' + todays)
            },
            clearData(){
                this.formDatas = ''
            }
        }
    }
</script>

<style>
    .disabled{
        background: aqua;

    }
    button{
        padding: 10px;
        margin: 10px;
        background: blueviolet;
        color: aliceblue;

    }
    input{
        width: 400px;
        padding: 8px;
        margin: 10px;
    }
</style>


