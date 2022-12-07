<template>
    <div class="bookbox">
        <div v-for="event in events" :key="event.id" >
            <BookItem :event="event"/>
        </div>
        
        <div class="class_Space"></div>
  
    </div>
    


</template>

<script>

    import BookItem from './BookItem.vue'


    export default{
        name: 'BookBox',
        components: {
            BookItem
        },
        props:{            
            events: Array
        }
    }

</script>

<style scoped>

.bookbox{
background-color: rgb(155, 195, 165);
display: grid;
grid-template-columns: 1fr 1fr;
padding: 25px;
margin:25px;
}


</style>