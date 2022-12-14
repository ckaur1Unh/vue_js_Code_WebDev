<template>
    <div>
        <img src="\unhicon.jpg">
        <h1> {{Organization}} </h1>
        <h4> {{titleName}} </h4>
    </div>
    <div class="Contact_Me">
    <h1> <button><a href="https://dull-jade-bat-hem.cyclic.app/"><b>Click here to know about me</b></a></button> </h1>
</div>
</template>
    
    <script>
    
    export default{
        name: 'HeaderTop',
        props:{
            Organization: String,
            titleName:String
        }
    }
    
    </script>
    
    <style scoped>
    
    div{
        text-align: center;
    }
    
    button{
    height:60px;
    width:200px;
    background-color: rgb(155, 195, 165);
    text-align: center;
    text-decoration: none;
    border-radius: 40%;
}
a{
    text-decoration: none;
    color:black
}
    </style>
