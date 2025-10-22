<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
                input: "",
            }
        },
        methods: {
            del(i){
                if (i > -1){
                    this.items.splice(i, 1);
                }
            },

            add(){
                if (this.input != ""){
                    this.items.push(this.input)
                }
            }
        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <ul>
        <li v-for="item,index in items" :key="index" :value="item">{{ item }} <button @click="del(index)">Delete</button></li>
        
    </ul>
    <!-- TODO: Add Code Here -->
    <input type="text" v-model="input"><button @click="add">Add!</button>
   
</template>
