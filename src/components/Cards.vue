<template>
    <div class="card">
        <a :href="url" target="_blank">
        <img :src="img_url" :alt="title + ' Poster'" />
        <h3>{{ title }}</h3>
        </a>
    </div>
</template>

<script>
export default {
    props: ['title','img_url','url']
};
</script>

<style>
    .card {
        flex: 1 1 33%;
        width: 33%;
        max-width: 33%;
        padding: 0px 8px;
        margin-bottom: 16px;
    }
    img {
        width: 100%;
        height: 300px;
        object-fit: cover;
        border-radius: 16px;
        box-shadow: 0px 4px 8px rgba(0, 0, 0, 0.15);
        transition: 0.4s;
    }
    h3 {
        padding: 16px;
        color: #313131;
        transition: 0.4s;
    }
    img:hover {
        transform: scale(1.05);
    }
    h3:hover {
        color: #24c444;
    }
</style>
