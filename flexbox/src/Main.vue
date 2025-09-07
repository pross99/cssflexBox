<script setup>

</script>

<template>
<section>

    <div class="s-container">
        <h1>
            We are flex 1
        </h1>
         <code> flex </code>
          <p>
          keyword uses <code>flex-grow flex-shrink and flex-basis</code>, meaning setting the flex value to 1, we are setting all three to default values
        </p>
        <p>
           <code> flex: 1</code> is the same as saying "flex-grow": 1, "flex-shrink: 1" "flex-basis: 100%"
        </p>

        <button id="flex1">
            I use flex 1
        </button>
    </div>

    <div class="s-container">
         <h1>
            We are flex 1
        </h1>
            <p>
            <code>flex-shrink </code> can be adjusted in case you'd want one element or container to shrink more or less depending on the available space
        </p>
            <div class="button-row">
          <button id="flex-shrink">
                I shrink first
            </button>
             <button id="flex-shrink0">
                I will not shrink!
            </button>
            </div>
    </div>


    <div class="s-container">
         <h1>
            We are flex 1
        </h1>
           <p>
            flex-grow allows the components to grow with the container
            </p>
              <div class="button-row">
            <button id="flex-grow">
                I use flex grow
            </button>
             <button id="flex-grow5">
                I will grow 5 times faster
            </button>
            </div>
    </div>

    <div class="s-container">
         <h1>
            We are flex 1
        </h1>
         <p>
            flex-basis is a way of setting the base width regardless of how much space is left in the container
        </p>

         <button id="flex-basis">
                I use flex basis, meaning i wont go above the width set in the flex basis rule
            </button>
    </div>

    <div class="s-text" id="svh">
         <h1>
            Hi There! With flex, I can easily adapt to screen widths. The following div is 100svh
        </h1>
        <p>
            Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
            Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, 
            when an unknown printer took a galley of type and scrambled it to make a type specimen book. 
            It has survived not only five centuries.
        </p>
    </div>

    <div class="s-text" id="lvh">
        <h1>
             Hi There! With flex, I can easily adapt to screen widths. The following div is 100lvh
        </h1>
          <p>
            Lorem Ipsum is simply dummy text of the printing and typesetting industry. 
            Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, 
            when an unknown printer took a galley of type and scrambled it to make a type specimen book. 
          </p>
    </div>
</section>



<section>
    <div class="s-container">
        <h1> So why is the normal vw & vh troublesome?</h1>
        <p> Phone UIs will have a browser that will take up space when landing on the home page. Also, when you scroll down the browser UI will become smaller, taking up less space. dvh and & dvh is also an option. However, many articles recommends not using this mesurment due to it being unstable EVEN WHEN THE viewport itself is unchanged.</p>
    </div>
</section>

</template>

<style scoped lang="scss">
    section {
        display: flex;
        flex-wrap: wrap;
        flex-direction: flex;
        background-color: lightgray;
        padding-top: 5em;
        
    }

    .s-container {
        flex: 1;
        flex-wrap: wrap;
        justify-content: center;
         padding: 1rem;
    border-radius: 1rem;
    background-color: beige;
        display: flex;
        margin: 0 0.2em;

        h1{
            
            flex: 1 1 100%;
           flex-wrap: wrap;
           display: flex;
           justify-content: center;
        }

        p{
            flex: 1 1 100%;
           flex-wrap: wrap;
           display: flex;
           justify-content: left;
           padding: 0 2em;
        }
       
    }

    .button-row{
        display: flex;
        flex-wrap: nowrap;
    }

    .s-text{
        background-color: lightblue;
        display: flex;
        justify-content: center;
        text-align: center;
        flex-wrap: wrap;
        h1{
            display: flex;
            width: 100%;
            justify-content: center;
            padding: 0.1em;
        }

        p{
            padding: 0px 0.5em;
            text-align: left;
            
        }
    }

 

    #flex1{
        flex: 1;
    }

    #flex-grow{
        flex-grow: 1;
    }
    #flex-grow5{
        flex-grow: 5;
    } 

    #flex-basis{
        flex-basis: 50%;
    }


    #flex-shrink{
        flex-shrink: 1;
        flex-grow: 1;
       
    }
    #flex-shrink0{
        flex-shrink: 2;
        flex-grow: 1;
    
    }

    #svh{
        width: 100svw;
        height: 100svh;
        border: solid 1px blueviolet;
    }

    #lvh{
        width: 100lvw;
        height: 100lvh;
        border: solid 1px red;
    }
</style>