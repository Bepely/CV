<script>
import { text } from "svelte/internal";


    export let showLearnPath = false;
    let textArray = [
        `Я познакомился с программированием в 2016 году, изучая игровой движок Unity. 
    На тот момент я не углубился в языки программирования и предпочел "Визуальный кодинг".`,
        `Одновременно с этим, я начал знакомится с PHP, так как хотел создать BackEnd для своего
    проекта, но дальше азов не продвинулся, не имея общего представления и понимания.`,
        `После этого у меня был длительный перерыв без прогресса в этой отрасли, пока мою сферу 
        деятельности не настиг ковид в начале 2020 года.`,
        `Основательно начал изучение Web программирования с апреля 2020, с помощью интернет ресурсов. В основе моего обучения стоял FreeCodeCamp`,
        `На данный момент я освоил HTML, CSS, JS, NodeJS, Svelte, в достаточном для личного использования, объеме.
        Имею общее представление о Frond-End фреймворках React и Vue, а так же Back-end фреймворке Express.`,
        `В моих планах присоединиться к команде разработчиков и работать над реальными проектами.`,
        `В дальнейшем планирую изучение Solidity, углубление в Blockchain и реализацию своего проекта.`
    ]

    let currentSlide = 0;
    function checkSlides(){
    if(currentSlide == textArray.length){
        currentSlide = 0;
    }
    if(currentSlide == -1){
        currentSlide = textArray.length -1;
    }
}


    function previousSlide() {
            currentSlide = currentSlide - 1;
            checkSlides();     
    }
    function nextSlide() {
            currentSlide = currentSlide + 1;
            checkSlides();     
    }

</script>



<div id="sliderText">
<button on:click={previousSlide} class="navShow">←</button>
<div id="textDisplay">
<h4>{currentSlide+1}/{textArray.length}</h4>
<p>{textArray[currentSlide]}</p>
</div>
<button on:click={nextSlide} class="navShow">→</button>
</div>

<style>
.navShow{
    border: 1px sold black;
    border-radius: 50%;
    width: 40px;
    height: 40px;
}
#sliderText{
    display: grid;
    grid-template-columns: 40px 1fr 40px;
    place-items: center;
    height: 220px;
}
#textDisplay{
    text-align: center;
}

    
</style>