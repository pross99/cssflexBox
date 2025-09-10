<script setup>
import src from '../public/img/book.png'
</script>

<template>
    <nav >
        <div class="nav-containers" >
            <img :src id="logo"/>
            <p> BookenHagen My parent container uses flex to display content respnsively.</p>
            
        </div>

        <div class="nav-containers">
            <button class="btn">
                we are responsive
            </button>
            <button>
                I am not
            </button>
        </div>
    </nav>


</template>

<style lang="scss" >

nav {
    display: flex;
    flex: 1;
    flex-wrap: wrap;
    background-color: beige;
}

.nav-containers{
    flex: 1;
    flex-wrap: wrap;
    border: solid 1px red;
   
    display: flex;
    justify-content: center;
    align-items: center;

    .btn{
        margin-left: auto;
        max-width: 20rem;
        flex: 1;
    }

 
}

#logo{

    width: 40px;
    height: 40;
}




</style>