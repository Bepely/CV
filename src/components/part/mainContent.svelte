<script>
import ListText from "../reusable/listText.svelte"
import TextSlider from "./textSlider.svelte"
import { fly } from 'svelte/transition'
let showLearnPath = false;

</script>
<!-- -->
<header>
    <h1>Николай Гогин </h1>
</header>
<mainContent>
<!-- Основная информация -->
<div id="mainDetails" class="block">
    
    <div class="details">
        <h3> Основная Информация</h3>
    <ListText fp="Занятость:" sp="Полная"/>
    <ListText fp="График работы:" sp="Полный День"/>
    <ListText fp="Желаемая зарплата:" sp="30 000 руб."/>
    <ListText fp="Телефон:" sp="+7 (903) 017-92-29"/>
    <ListText fp="Электронная почта:" sp="ngogin7@gmail.com"/>
    <ListText fp="Telegram:" sp="@bepely"/>
</div>
</div>

<!--Личная информация -->
<div id="personal" class="block"> 
    
    <div  class="details">
        <h3>Личная Информация</h3>
    <ListText fp="Гражданство:" sp="РФ"/>
    <ListText fp="Место проживания:" sp="г. Москва"/>
    <ListText fp="Образование:" sp="Неполное Высшее"/>
    <ListText fp="Дата рождения:" sp="7 Января 1998 (23 года)"/>
    <ListText fp="Пол:" sp="Мужской"/>
    <ListText fp="Семейное положение:" sp="Гражданский брак"/>
    <ListText fp="Дети:" sp="Нет"/>
</div>
</div>

<!--Опыт работы-->
<div id="experience" class="block">
    
    <div id="expJob" class="details">
        <h3>Опыт Работы</h3>
            <ListText fp="Агент по релокации:" sp="10.2017 - 12.2019"
            details="Работа с иностранными клиентами, переезжающими в Москву. Поиск квартир, проведение переговоров, составление двуязычных документов. Из достижений - работа с посольствами Египта и Туниса."/>
            <ListText fp="Повар:" sp="10.2019 - 12.2020"
            details="Работал поваром в разных заведениях. Главными достижениями считаю работу частным поваром у носителей английского языка и работу шефом в крафтовом баре." />
        </div>
    
    
</div>

<!--Образование-->
<div id="education" class="block">
    
    <div id="expJob" class="details">
        <h3>Образование</h3>
            <ListText fp="ГУУ:" sp="2014-2015"
            details="Окончил 1 курс Государственного и Муниципального управления, после чего пошел работать. На данный момент обучение приостановлено."/>
            <ListText fp="Колледж Царицыно:" sp="2017"
            details="Отучился на повара и кондитера 4 разряда 🙄" />
            </div>   
</div>
<!--Изучение Программирования-->
<div id="programming" class="block">
<h3>Изучение Программирования</h3>
<TextSlider showLearnPath={showLearnPath} />

</div>
<!-- Дополнительная Информация-->
<div id="additional" class="block">
    
        <div id="addInfo" class="details">
            <h3>Дополнительная информация</h3>
            <ListText fp="Иностранный язык:" sp="Английский"/>
            <ListText fp="Технологии:" sp="HTML, CSS, JS, Svelte, NodeJS"/>
            <ListText fp="Хобби:" sp="Музыка"/>
            <ListText fp="Личные качества:" sp="Активность, инициативность, предприимчивость" />

        </div>




</div>





</mainContent>

<style>

header{
    display: grid;
    place-items: center;
}

.block{
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
}
.details{
    text-align: center;
}


@media (min-width: 1000px){
    header>h1{
        margin: 0;
        display: inline-block;
    }
    .block{
        max-width: 450px;
        height: 100%;
        margin: 0;
        padding: 10px;
        


    }
    mainContent{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        place-items: center;
    }
    header{
        place-items: center;
    }
}


    
</style>