<template>
<div>
    <div>
        <input v-model="name" type="text" >
        {{ name }}
    </div>
    <div>
        <input v-model="user.first_name" type="text" >
    </div>
    <div>
        <input v-model="user.last_name" type="text" >
    </div>
    <div>
         {{ user.first_name + user.last_name}}
    </div>
    <div>
        <select name="" id="" v-model="pageCount">
            <option value="5">5</option>
            <option value="10">10</option>
            <option value="15">15</option>
        </select>
    </div>
</div>
</template>

<script>
export default {
    name: 'ObservadoresVue',
    data() {
        return {
            name: '',
            pageCount: 5,
            user: {
                first_name: '',
                last_name: ''
            }
        }
    },

    watch: {
        name(newValue){
            if(newValue.length >= 3) {
                this.saveUserName();
            }
        },
        pageCount(){
            this.changePage();
        },
        user: {
            handler(){
                console.log('alterado');
            },
            depp: true
        }
    },
    computed: {

    },
    methods: {
        saveUserName(){
            console.log('ajax');
            console.log(this.name);
        },
        changePage(){
            console.log('Ajax change page');
        }
    }
}
</script>