<template>
  <div>

      <h1>{{ fullName }}</h1>    
      <input type="text" v-model="firstName" style="color: #fff; border:1px solid #fff">
      <input type="text" v-model="lastName" style="color: #fff; border:1px solid #fff">
      <h1 v-if="firstName">{{firstName}}</h1>
      <h1 v-else>firstName is Empty</h1>
      <div>
        <h1 v-if="personal.books.length > 0 ">{{personal.books[0]}}{{personal.books[1]}}{{personal.books[2]}}</h1>
        <h1 v-else>this Book value isn't Equal to 3</h1>
        <h1 v-if="personal.books[0] === 'English' ">{{personal.books[0]}} </h1>
        <h1 v-for=" books in personal.books" :key="books.id">{{books}} {{books.id}}</h1>
      </div>
  </div>
</template>

<script>
export default {
  name:'NuxtTutorial',
  data(){
    return{
        firstName:"Faizan",
        lastName:"Khan",
      personal:{
        authorname:"Faizan",
        books:[
          "English",
          "Physics",
          "Chemistry",
        ]
      }
    }
  },
  mounted(){
    this.firstName = "Faizan Dev"
    this.personal.books = [
          "Urdu",
          "Physics",
          "Chemistry",
    ]

    
  },
  computed:{
    fullName(){
      return this.firstName +""+ this.lastName
    }

  }
}

</script>
