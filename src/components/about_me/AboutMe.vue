<template>
    <div class="about_me" id='page2'>
        <div class="container">
        <h1 class="h1">Обо мне</h1>
            <div
                data-aos-offset="300"
                data-aos="fade-right"
                class="card content_block"
            >
                <ul class="">
                    <li>в самом начале своего обучения, проходил курсы на htmlacademy.ru</li>
                    <li>пользуюсь сервисом codewars.com;</li>
                    <li>использую React и Vue 3, недавно начал изучать Next.js;</li>
                    <li>HTML5, CSS3, JavaScript;</li>
                    <li>pinia, redux, vuex;</li>
                    <li>jira, github;</li>
                    <li>одни из библиотек которые использую: tailblocks.cc, reactbootstrap;
                tailwindcomponents, tailwindcss, reactbootstrap, bootstrap;</li>
                    <li>есть опыт работы с макетами в Figma;</li>
                </ul>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>

.about_me {
    width: 100%;
    height: 800px;
    background-color: #ebebeb;
    overflow: hidden;
}

.content_block {
    padding: 50px;
    background-color: #fff;
    border-radius: 10px;
    margin-top: 50px;
}

li {
    font-size: 18px;
    list-style: inside;
}

h1 {
    text-align: center;
}

@media screen and (max-width: 520px) {
  .about_me {
    height: 100%;
  }
}

</style>