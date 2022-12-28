<template>
    <div>
        <div class="home background">
            <div class="text_content container">
                <p>Привет! Меня зовут Владислав, я -</p>
                <h1>FRONTEND РАЗРАБОТЧИК</h1>
                <a href="#page1"><div class="arrow-down">
                    <span></span>
                    <span></span>
                    <span></span>
                </div></a>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style scoped>
.arrow-down {
    margin: 30px;
}
.arrow-down span {
    display: block;
    width: 30px;
    height: 30px;
    border-bottom: 5px solid #fdfdfd;
    border-right: 5px solid #337AB7;
    transform: rotate(45deg);
    margin: -16px;
    animation: arrow-down 2s infinite;
}
.arrow-down span:nth-child(2){
    animation-delay: -0.2s;
}
.arrow-down span:nth-child(3){
    animation-delay: -0.4s;
}
@keyframes arrow-down {
    0%{
        opacity: 0;
        transform: rotate(45deg) translate(-20px,-20px);
    }
    50%{
        opacity: 1;
    }
    100%{
        opacity: 0;
        transform: rotate(45deg) translate(20px,20px);
    }
}  
.background {
    background: url('../../img/cvbcvbvb.jpg')  center center/cover no-repeat;
    max-width: 100%;
    height: 100vh;
    background-attachment: fixed;
}

.text_content {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    max-width: 100%;
    height: 100vh;
    background: rgba(0, 0, 0, 0.4)
}

h1 {
    color: #fff;
}

p {
    color: #fff;
}

@media screen and (max-width: 520px) {
  h1 {
    text-align: center;
  }
  p {
    text-align: center;
  }
}

</style>