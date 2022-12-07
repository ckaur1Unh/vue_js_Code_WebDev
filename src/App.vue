<template>
  <div class="container">
    
    <HeaderTop Organization="University Of New Haven" titleName="Events Calender" />
    <BookBox :events="events" />
    
</div>
</template>

<script>

import HeaderTop from './components/HeaderTop.vue'
import BookBox from './components/BookBox.vue' 

export default {
  name: 'App',
  components: {    
    HeaderTop,
    BookBox
  },

  data(){
    return {
      events: []
    }

  },

  methods: {

    // promises

      async fetchEvents(){
          const res = await fetch('https://itchy-lingerie-deer.cyclic.app/api')
          const data = await res.json()
          console.log( data.events )
          return data.events
      }

  },
  async created(){
    this.events = await this.fetchEvents()
  }
}

</script>

<style>

@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 1200px;
  margin: 30px auto;
  overflow: auto;
  min-height: 500px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;
}
img{
  width: 80px;
  height: 80px;
}

</style>
