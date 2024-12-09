<template>
<div>
    <h1 className="appName"> {{appName}} </h1>
    <h2 class="welcome">Welcome to the Art of Digital World</h2>
</div>
</template>

<script>

export default{
    name: 'MyHeader',
    props:{ 
        appName:String
    }
}

</script>

<style scoped>

div{
    text-align: center;
}
.appName{
    padding: 1rem 0;
    margin-bottom: 1.5rem;
    /* background-color:  #ff6b22; */
    background-color: #CCFF00;
    color: #2e2e2e;
    border-radius: 10px;
}

.welcome{
    color: #CCFF00;
    font-size: 2rem;
    margin-bottom: 1.5rem;
    background-color: rgb(10, 12, 13);
    border-radius: 10px;
    padding: 2rem 3rem;
    box-sizing: border-box;
    display: inline-block; 
    transition: all ease 0.3s;

}

@media screen and (max-width:750px) {
    .welcome{
        font-size: 1.2rem;
    }
    
}

</style>