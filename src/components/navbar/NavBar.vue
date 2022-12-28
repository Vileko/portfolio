<template>
    <header>
        <ul class="nav-bar container" id='page1'>
            <li><a href="#">Главная</a></li>
            <li><a href="#page2">Обо мне</a></li>
            <li><a href="#my_project">Портфолио</a></li>
            <li><a href="#work">Работа</a></li>
        </ul>
    </header>
</template>

<style scoped>
.container {
    padding: 0;
}

header {
    background-color: #fff;
}

.nav-bar {
    display: flex;
    justify-content: center;
}

li {
    padding: 25px;
}

a {
    color: rgb(0, 0, 0);
}

@media screen and (max-width: 520px) {
  li {
    padding: 10px;
    font-size: 12px;
  }
}
</style>