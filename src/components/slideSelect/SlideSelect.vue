<template>
    <div id="SequenceSelect">
        <div class="title">slides</div>
        <Slide
            v-for="slide in availableSlides"
            :key="slide.slide"
            :slide="slide"
        />
    </div>
</template>

<script>
import Slide from './Slide.vue';

export default {
    props: {
        availableSlides: Array
    },
    components: {
        Slide
    }
};
</script>

<style scoped>
#SequenceSelect {
    margin-left: 40px;
    flex: 1;
    border: 2px solid black;
    display: flex;
    flex-direction: column;
}

.title {
    display: flex;
    background-color: lightgray;
    color: #34373a;
    justify-content: center;
    align-items: center;
    height: 30px;
}
</style>
