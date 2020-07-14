<template>
    <div draggable="true" @dragstart="dragStart" class="slide">
        {{ slide.slide }}
    </div>
</template>

<script>
export default {
    props: {
        slide: Object
    },
    methods: {
        dragStart(e) {
            e.dataTransfer.setData('slide', JSON.stringify(this.slide));
        }
    }
};
</script>

<style scoped>
.slide {
    color: #34373a;
    padding: 5px;
}
</style>
