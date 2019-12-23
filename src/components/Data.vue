<template>
    <div>
        <div v-bind:style="divStyle">
            <p v-bind:style="{color:textColor, textTransform: upperText, background:bgColor}">My VueJS paragraph</p>
        </div>
        <div>
            <h3>Conditional Binding</h3>
            <div v-if="myDate > 1 && myDate < 12">
                <p>Good Morning</p>
            </div>
            <div v-else-if="myDate >=12 && myDate < 18">
                <p>Good Afternoon</p>
            </div>
            <div v-else>
                <p>Good Evening</p>
            </div>
        </div>
        <div>
            <h3>List Rendering</h3>
            <div>
                <ul v-for="task in myTasks" :key="task.id">
                    <li>
                        {{task.name}}
                        <span v-if="task.completed">Completed</span> <span v-else>Not Completed</span>
                    </li>
                </ul>
            </div>
        </div>

    </div>
</template>

<script>
    export default {
        name: "Data",
        data(){
            const Dates = new Date();
            const myDate = Dates.getHours();
            return {
                divStyle: {
                    padding:'100px' ,
                    background:'black',
                    textAlign:'center'
                },
                textColor: 'red',
                upperText: 'uppercase',
                bgColor: 'yellow',
                myDate: myDate,
                myTasks: {
                    task1:{
                        id:1,
                        name: 'task one',
                        completed: false
                    },
                    task2:{
                        id:2,
                        name: 'task two',
                        completed: false
                    },
                    task3:{
                        id:3,
                        name: 'task three',
                        completed: false
                    }
                }
        }
        }
    }
</script>

<style scoped>
ul{
    list-style: none;

}
    li{
        background: aqua;
        padding: 20px;
    }
    span{
        color: red;
    }
</style>
