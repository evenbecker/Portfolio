<template>
    
        <div class="container-fluid p-4">
            <label>Enter your name:</label>
            <input v-model="name" class="form-control" />
        </div>
        <h4 class="p-2 custom-margin">
            {{name}}'s To Do List
        </h4>
        <div class="container-fluid p-4">
            <div class="row" v-if="filteredTasks.length == 0">
                <div class="col text-center">
                    <b>Nothing to do. Let's listen to some music.</b>
                </div>
            </div>
            <template v-else>
                <div class="row">
                    <div class="col font-weight-bold"><u>Tasks:</u></div>
                    <div class="col-2 font-weight-bold"><u>Done?</u></div>
                </div>
                <div class="row" v-for="t in filteredTasks" v-bind:key="t.action">
                    <div class="col">{{t.action}}</div>
                    <div class="col-2 text-center">
                        <input type="checkbox" v-model="t.done" 
                             class="form-check-input" />
                    </div>
                </div>
            </template>
            <div class="row py-2">
                <div class="col-9">
                    <input v-model="newItemText" class="form-control" />
                </div>
                <div class="col-3">
                    <button class="btn btn-primary" 
                        v-on:click="addNewTodo">Add</button>
                </div>
            </div>
            <div class="row py-2">
                <div class="col">
                    <!--<input type="checkbox" v-model="hideCompleted" 
                        class="form-check-input" />
                    <label class="form-check-label font-weight-bold">
                        Hide completed tasks
                    </label>-->
                    <div class="form-check form-switch">
                    <input class="form-check-input" type="checkbox" v-model="hideCompleted" id="flexSwitchCheckChecked" checked>
                    <label class="form-check-label" for="flexSwitchCheckChecked">Hide completed tasks</label>
                    </div>
                </div>
            </div>
            <div class="row py-2">
                <div class="col">
                    <div class="myWidth">
                    <button class="btn btn-sm btn-warning" 
                            v-on:click="deleteCompleted">
                        <b>Delete Completed</b>
                    </button>
                </div>
                </div>
            </div>
        </div>
    
</template>

<script>

    export default {
        name: 'Todo1',
        data() {
            return {
                name: "Even",
                tasks: [],
                hideCompleted: true,
                newItemText: ""
            }
        },
        computed: {
            filteredTasks() {
                return this.hideCompleted ?
                    this.tasks.filter(t => !t.done) : this.tasks
            }
        },
        methods: {
            addNewTodo() {
                this.tasks.push({
                    action: this.newItemText,
                    done: false
                });
                this.storeData();
                this.newItemText = "";
            },
            storeData() {
                localStorage.setItem("todos", JSON.stringify(this.tasks));
            },
            deleteCompleted() {
                this.tasks = this.tasks.filter(t => !t.done);
                this.storeData();
            }
        },
        created() {
            let data = localStorage.getItem("todos");
            if (data != null) {
                this.tasks = JSON.parse(data);
            }
        }
    }
</script>
<style scoped>
.myWidth{
    width: 50%;
}
.custom-margin{
    margin-left : 15px;
}
</style>