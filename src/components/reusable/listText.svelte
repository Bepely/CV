<script>
    import { createEventDispatcher } from 'svelte';
    const dispatch = createEventDispatcher();
export let fp;
export let sp;
export let details = "none";
let showedDetails = false;

function showDetails(){
    showedDetails = !showedDetails;
}

</script>
<item>
<p id="fp">{fp}</p>
<p id="sp">{sp}</p>
{#if details!=="none"}
    {#if showedDetails==true}
    <p id="showedText">{details}</p>
    <button
     on:click={showDetails}
     id="buttonToShow"
     style="background-color: salmon;"
     >Скрыть</button>
       
        {:else}
        <button
        on:click={showDetails} 
        id="buttonToShow"
        >Подробнее</button>
    {/if}
   

{/if}



<!--<details id="details">
        <summary>Подробнее</summary>
        <p>{details}</p>
    </details>-->

</item>

<style>
#fp{
    text-align: right;
}
#sp{
    text-align: center;
}

item{
    display: grid;
    grid-template-columns: 1fr 1fr;
    place-items: center;
    grid-template-areas: "a b"
                         "c c"
                         "d d";
    border-bottom: 1px solid salmon;
}
#buttonToHide{
    grid-area: c;
    text-align: center;
    padding-bottom: 5px;
  
}
#buttonToShow{
    grid-area: d;
    text-align: center;
    padding-bottom: 5px;
}
#showedText{
    grid-area: c;
    text-align: center;
    padding-bottom: 5px;
}


</style>