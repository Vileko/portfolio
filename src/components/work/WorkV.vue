<template>
    <div class="work" id='work'>
        <div class="container">
            <h1>Работа</h1>
            <div class="blocks"> 
                <div v-for="p in work" :key="p.id" >
                    <div
                        data-aos="fade-right"
                        class="card block"
                        data-aos-offset="300"
                    >
                        <div class="block_1">
                            <img :src="p.img" alt="foto" class="img">
                            <div class="block_text">
                                <div 
                                    ata-aos-offset="300" 
                                    data-aos="fade-right"
                                    data-aos-duration="1500"
                                    class="style_line_min"
                                ></div>
                                <h3 data-aos="zoom-in">{{p.b1}}</h3>
                                <div>
                                    <h3 data-aos="zoom-in">библиотеки:</h3> 
                                    <div  class="libraries">
                                        <p v-for="b in p.b2" :key="b.id">
                                            <span data-aos="zoom-in">{{b}}</span>
                                        </p>
                                    </div>
                                </div>
                                <button class="btn_1000px">
                                    <a :href="p.url">Смотреть</a>
                                </button>
                            </div>
                        </div>
                        <div class="block_2">
                            <div class="description">
                                <div 
                                    ata-aos-offset="300" 
                                    data-aos="fade-right"
                                    data-aos-duration="1500"
                                    class="style_line"
                                ></div>
                                <div class="block_description">
                                    <h3 data-aos="zoom-in" class="h3">Дополнительные инструменты:</h3>
                                    <div data-aos="zoom-in" v-for="b in p.b3" :key="b.id">
                                        <li class="li">{{b}}</li>
                                    </div>
                                    <h3 data-aos="zoom-in" class="h3">Что сделанно из последнего:</h3>
                                    <div data-aos="zoom-in" v-for="text in p.b4" :key='text.id'>
                                        <li>{{text}}</li>
                                    </div>
                                    <button 
                                        data-aos-offset="0"
                                        data-aos="zoom-in" 
                                        class="btn_900px"
                                    >
                                        <a :href="p.url">Смотреть</a>
                                    </button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import img_0 from '../../img/game.jpg';
    export default {
        data() {
            return {
                    work: [
                        {
                            id: 1, 
                                url: 'https://gamelit.ru/', 
                                img: img_0,
                                b1: 'Интернет магазин',
                                b2: ['React', 'Redux', 'Next.js', 'tailblocks.cc', 'reactbootstrap','tailwindcomponents','tailwindcss'],
                                b3: ['Jira', 'GitHub'],
                                b4: [
                                    'создавал адаптивную верстку сайта;',
                                    'внедрил библиотеку с фотогалереей и полностью адаптировал ее под сайт. Полностью настроил открытие фотографии на полный экран и легкое сворачивание фотографии при клике на пустое место;',
                                    ' внедрил бургер и полностью его адаптировал под все размеры;',
                                    'также делал много разных правок по сайту.'
                                ]
                        }],
            }
        },
    }
</script>

<style scoped>
.work {
    background-color: rgb(47, 87, 218);
    height: 100%;
}

.block_description {
    padding: 15px 25px;
}

.style_line {
    width: 550px;
    height: 1px;
    background-color: rgb(255, 255, 255);
    margin: 0 auto;
}

.h3 {
    text-align: center;
    color: #fff;
}

.block {
    border: 1px solid rgb(255, 255, 255);
    padding: 15px;
    margin: 0 auto;
    width: 850px;
    height: 800px;
    margin-top: 50px;
   
}

.block_1 {
    display: flex;
    transition: .4s;
    height: 400px;
}

.block_2 {
    margin-top: 50px;
}

.block:hover {
    transition: .4s;
    box-shadow: 10px 5px 5px #fff;
}

.block_text {
    display: flex;
    flex-direction: column;
    margin-left: 50px;
    height: 100%;
    width: 100%;
    justify-content: space-between;
    border-left: 1px solid #fff;
    padding-left: 15px;
}

.img {
    width: 600px;
    height: 400px;
}


.libraries p {
    margin-top: 10px;
}

.libraries p span{
    width: 100%;
    border: 1px solid #fff;
    border-radius: 10px;
    padding: 2px 10px;
}

h3 {
    color: #fff;
    margin: 0;
}

button {
    border: none;
    padding: 0;
}

a {
    display: block;
    padding: 15px;
    font-size: 16px;
    color: rgb(8, 8, 8);
    transition: .4s;
}

a:hover {
    background-color: #c4c4c4;
}

span {
    color: #fff;
}

h1 {
    color: #fff;
    text-align: center;
}

li {
    list-style: disc;
    color: #fff;
}

.style_line_min {
    display: none;
}

.btn_900px {
    display: none;
}

@media screen and (max-width: 990px) {
    .container {
        padding: 15px;
    }
    .block {
        margin: 0 auto;
        max-width: 600px;
        height: 100%;
    }
    .block_1 {
        flex-direction: column;
        height: 500px;
    }
    .img {
        max-width: 100%;
    }

    .block_text {
        margin: 0;
        padding: 0;
        border: none;
        justify-content: start;
    }

    .libraries {
        justify-content: center;
        display: flex;
        flex-wrap: wrap;
    }

    .libraries p{
        padding: 2px;
    }

    h3 {
        text-align: center;
    }

    .btn_1000px{
        display: none;
    }
    .btn_900px {
        display: flex;
        justify-content: center;
        width: 100%;
        margin-top: 25px;
    }


    .style_line{
        display: none;
    }

    .style_line_min {
        width: 500px;
        height: 1px;
        background-color: #fff;
        display: block;
        margin: 0 auto;
        margin-top: 25px;
        margin-bottom: 15px;
    }

    .block_2 {
        max-width: 600px;
        margin: 0;
        margin-top: 15px;
    }
}

@media screen and (max-width: 669px) { 
    .block {
        max-width: 100%;
        padding: 0;
    }
    .style_line_min {
        max-width: 250px;
    }
    .img {
        max-width: 100%;
    }
}

@media screen and (max-width: 540px) { 
        .block_1 {
        height: 450px;
    }
}

</style>