<template>
    <div>

        <h1 :class="{ 'title': true, 'title-home': isHome}">
            Curso VUE 3
        </h1>
        <p :class="pClass">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Explicabo est fugit debitis perspiciatis blanditiis aliquam iusto molestias rerum tempora, doloremque quis nihil accusamus at delectus. Earum blanditiis dolores asperiores maiores.</p>
        
        <p :style="styleClass">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Explicabo est fugit debitis perspiciatis blanditiis aliquam iusto molestias rerum tempora, doloremque quis nihil accusamus at delectus. Earum blanditiis dolores asperiores maiores.</p>
        
        <div v-for="obj in todos" :key="obj.id">
            <img v-if="obj.imgSrc"
                :src="obj.imgSrc" alt="">
            <p>{{ obj.title }}</p>
        </div>

    </div>
</template>

<script>
export default {
    name: 'TheHeader',
    data(){
        return {
            isHome: false,
            classVar: 'classVar',
            pClass: ['text', 'text-home'],
            styleClass: { color: 'aqua', backgroundColor: 'black'},
            imgAlt: 'Foto de Jon Snow',
            todos: [
                {
                "userId": 1,
                "id": 1,
                "title": "delectus aut autem",
                "completed": false,
                "imgSrc": 'https://via.placeholder.com/150',
                },
                {
                "userId": 1,
                "id": 2,
                "title": "quis ut nam facilis et officia qui",
                "completed": false,
                "imgSrc": 'https://via.placeholder.com/150',
                },
                {
                "userId": 1,
                "id": 3,
                "title": "fugiat veniam minus",
                "completed": false
                },
                {
                "userId": 1,
                "id": 4,
                "title": "et porro tempora",
                "completed": true
                },
                {
                "userId": 1,
                "id": 5,
                "title": "laboriosam mollitia et enim quasi adipisci quia provident illum",
                "completed": false
                }
            ]
        }
    }
}
</script>

<style>
.todos-item {
    background: #000;
}
    .header {
        background: #000;
        color: #fff;
    }

    .title {
        font-size: 20px;
        color: blue;
    }

    .title-home {
        font-size: 40px;
        color: green;
    }

    .text {
        color: yellow;
    }

    .text-home {
        color: #42b983;
    }
</style>