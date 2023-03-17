<template>
    <div>
        <div v-for="item in items"> 
            <h1>{{ item.message }}</h1>
        </div>
        <p>De structure</p>
        <li v-for="(item,index) in items">{{ parentMessage }}  {{ index }} {{ item.message }}  </li> <br /> <br />
        <li v-for="(value,key,index) in myObjects"> {{ index }} {{ key }}: {{ value }}</li>
        
    </div>
</template>
<script>
    export default {
        name:'ForLoop',
        data(){
            return{
                parentMessage:'Parent Message',
                items:[
                    {
                        message:'foo',

                    },
                    {
                        message:'bar'
                    }
                ],
                myObjects:{
                    title:'how to do lists in Vue',
                    author: 'Jane Doe',
                    publishedAt: '2016-04-10'
                },

                
            }
            
        }
    }


</script>