<template>
    <div class="my_works" id='my_project'>
        <div class="container">
            <h1 class="h1">Портфолио</h1>
            <div class="blocks"> 
                <div 
                    data-aos-offset="300"
                    data-aos="fade-right"
                    class="card content_block"
                    v-for="p in post" 
                    :key="p.id" 
                >
                    <div class="block">
                        <img :src="p.img" alt="foto" class="img">
                        <div class="block_text">
                            <div class="style_line_width_990"></div>
                            <h3 class="h3">{{p.b1}}</h3>
                            <div>
                                <h3>библиотеки:</h3> 
                                <div class="libraries">
                                    <p v-for="b in p.b2" :key="b.id">
                                        <span>{{b}}</span>
                                    </p>
                                </div>
                            </div>
                            <button>
                                <a :href="p.url">Смотреть</a>
                            </button>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>

<script>

import img_1 from '../../img/pizza.jpg';
import img_2 from '../../img/c.jpg';
import img_3 from '../../img/to-do.jpg';
import img_4 from '../../img/3.jpg';
import img_5 from '../../img/weather.jpg';

    export default {
        data() {
            return {
                post: [
                    {
                        id: 0, 
                        url: 'https://incandescent-dusk-b6acb8.netlify.app/', 
                        img: img_1,
                        b1: 'Интернет магазин',
                        b2: ['React', 'Router', 'React-bootstrap', 'Input-mask']
                    },
                    {
                        id: 1,
                        url: 'https://lustrous-melomakarona-9789b6.netlify.app',
                        img: img_5,
                        b1: 'Прогноз погоды',
                        b2: ['Vue 3', 'Axios']
                    },
                    {   id: 2, 
                        url: 'https://thunderous-souffle-926340.netlify.app/',
                        img: img_3,
                        b1: 'Список дел',
                        b2: ['Vue 3', 'Router', 'Анимация']
                    },
                    {   id: 3, 
                        url: 'https://taupe-seahorse-e2dcdf.netlify.app/',
                        img: img_4,
                        b1: 'Интернет магазин',
                        b2: ['Vue 3', 'Vuex','Router', 'Maska']
                    },
                    {
                        id: 4,
                        url: 'https://warm-salamander-680627.netlify.app/',
                        img: img_2,
                        b1: 'Калькулятор',
                        b2: ['Vue 3']
                    },
                    
                ],
                activeBlock: false
            }
        },
    }
</script>

<style  scoped>
.block {
    display: flex;
    margin-top: 50px;
    border: 1px solid #ebebeb;
    width: 850px;
    height: 400px;
    padding: 15px;
    transition: .4s;
    margin: 0 auto;
    margin-top: 25px;
}

.block:hover {
    box-shadow: 10px 5px 5px #d1d0d0;
}

.block_text {
    display: flex;
    flex-direction: column;
    margin-left: 50px;
    height: 100%;
    width: 100%;
    justify-content: space-between;
    border-left: 1px solid #ebebeb;
    padding-left: 15px;
}

.img {
    width: 600px;
}

h3 {
    margin: 0;
}

.libraries p span{
    width: 100%;
    border: 1px solid #c4c4c4;
    border-radius: 10px;
    padding: 2px 10px;
}

.libraries p {
    margin-top: 10px;
}

.style_line_width_990 {
    display: none;
}

@media screen and (max-width: 990px) {
    .block {
        flex-direction: column;
        height: 100%;
        max-width: 600px;
        padding: 0;
    }
    .block_text {
        margin-left: 0;
        border: none;
        justify-content: flex-start;
        padding: 0;
    }
    .img {
        max-width: 100%;
    }
    h3 {
        text-align: center;
    }
    .h3 {
        margin-top: 5px;
    }
    .libraries {
        display: flex;
        justify-content: center;
    }
    .libraries p {
        padding: 5px;
        margin-bottom: 15px;
    }
    .style_line_width_990 {
        display: block;
        width: 500px;
        height: 1px;
        background-color: #c4c4c4;
        margin: 0 auto;
        margin-top: 15px;
    }
    .container {
        padding: 15px;
    }
}

@media screen and (max-width: 669px) { 
    .block {
        flex-direction: column;
        height: 100%;
        max-width: 100%;
    }

    .style_line_width_990 {
        max-width: 65%;
    }
    .libraries {
        flex-wrap: wrap;
    }

    .libraries p {
        margin: 0px;
    }
    
    button {
        margin-top: 10px;
    }

    .img {
        max-width: 100%;
    }

}


button {
    border: none;
    padding: 0;
}

a {
    display: block;
    padding: 15px;
    font-size: 16px;
    color: #000;
    transition: .4s;
}

a:hover {
    background-color: #c4c4c4;
}
</style>