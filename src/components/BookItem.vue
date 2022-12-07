<template>
    
        <div class="container_1">            
        <div class="event">   
        <h2><b>{{event.title}}</b></h2>
        <h4> {{event.time}}</h4>
        <h4> {{event.location}}</h4>
        <h4> Seats: {{event.seats}}</h4>
        <h4> RSVP required: {{event.RSVP}}</h4>
        </div>
  
    </div>

</template>

<script>


export default{
    name: 'BookItem',
    props:{
        event: Array
    }
}


</script>

<style scoped>


h4{
    margin: 2px;
}
.container_1{
    width:auto;
    height:auto;
}
.event{
    border-radius: 50%;
    background-color: rgb(134, 167, 145);
    color: rgb(67, 35, 2);
    padding: 25px;
    border: 0.2em  rgb(1, 59, 22);
    margin: 30px;
    text-align: center;
}


</style>