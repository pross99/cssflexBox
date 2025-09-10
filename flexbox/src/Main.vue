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

    <div class="s-container shrink">
         <h1>
            We are flex 1
        </h1>
            <p>
            <code>flex-shrink </code> can be adjusted in case you'd want one element or container to shrink more or less depending on the available space
        </p>
            <div class="button-row">
          <button id="flex-shrink">
                I have flex-shrink 1
            </button>
             <button id="flex-shrink5">
                I have flex-shrink 5
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
            The following div is 100svh
        </h1>
        <p>
           A use case for 100svh if you have content that needs to be immediayely visible without scrolling, svh can be the better choice. 60 to 64 percent of all network traffic is from mobile phones.
           In conclusion: If you need to guarantee that elements are fully visible within the smallest viewport, svh ensures compatibility:
        </p>
    </div>

    <div class="s-text" id="lvh">
        <h1>
              The following div is 100lvh
        </h1>
          <p>
            So 100lvh ensures your element always stretches to the full screen size, even if it means some content might be hidden by browser UI. Used for consisent layouts
          </p>
    </div>
</section>



<section>
    <div class="s-text" id="dvw">
        <h1> I use 100dvw</h1>
        <p> Phone UIs will have a browser that will take up space when landing on the home page. Also, when you scroll down the browser UI will become smaller, taking up less space. dvh and & dvh is also an option. However, many some articles recommends not using this mesurment due to it being unstable EVEN WHEN THE viewport itself is unchanged, while others recommends it for mobile-first development</p>
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
        min-width: 300px;
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
        width: 400px;

        button{
        flex-grow: 1;
        padding: 1rem;
        border: 1px solid gray;
      

        &#flex-shrink{
                flex-shrink: 1;
       background-color: blue;
        }

        &#flex-shrink5{
                flex-shrink: 5;
                 background-color: red;
                }
            }
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

    #flex-shrink0{
        flex-shrink: 5;
        background-color: red;
    
    }

    #svh{
        width: 100svw;
        height: 100svh;
        border: solid 1px blueviolet;
        padding: 2svw;
    }

    #lvh{
        width: 100lvw;
        height: 100lvh;
         padding: 2lvw;
        border: solid 1px red;
        background-image: url(https://images.pexels.com/photos/406014/pexels-photo-406014.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1);
        background-repeat: no-repeat;
        background-position: center;
        background-size: cover;
    }

    #dvw{
        width: 100dvw;
         padding: 2dvw;
    }
</style>