<script>
import {onMount} from 'svelte'
let canvas;
let emoji = new Image;
emoji.src = "https://icons.iconarchive.com/icons/google/noto-emoji-animals-nature/256/22237-boar-icon.png";
console.log(emoji.src);
let width = window.innerWidth;
let height = window.innerHeight;
onMount(()=> {


const ctx = canvas.getContext('2d');


let point = [];

function getRandomPoint(){
    point = [];
    point.push(Math.floor(Math.random(height)*height));
    point.push(Math.floor(Math.random(width)*width)); 
    
}

function printEmoji(){
    getRandomPoint()
    console.log(point);   
    ctx.drawImage(emoji, point[1],point[0], 50, 50);
    setTimeout()
    
}





})




</script>
<canvas  
bind:this={canvas}
width={width}
height={height}>

</canvas>


<style>

canvas{
    width: 100vw;
    height: 100vh;
    z-index: -1;
    position: absolute;
}
    
</style>