<template>
    <div class="SingleSlideSetting">
        <div class="menuIcon">
            <div class="menuBar"></div>
            <div class="menuBar"></div>
            <div class="menuBar"></div>
        </div>
        <input
            type="number"
            v-model.number="slideData.duration"
            class="time setting"
        />
        <div class="slide setting">{{ slideData.slide }}</div>
        <select v-model="slideData.transitionToNext" class="transition setting">
            <option value="cut">cut</option>
        </select>
    </div>
</template>

<script>
export default {
    props: {
        slideData: Object
    },
    methods: {}
};
</script>

<style scoped>
.SingleSlideSetting {
    display: flex;
    width: 100%;
    align-items: center;
    height: 60px;
    padding: 0 10px;
    margin-bottom: 10px;
    cursor: move;
    border-radius: 5px;
}

.setting {
    padding: 10px;
    background-color: #5e5e5e;
    color: white;
    border-radius: 7px;
    font-size: 20px;
    text-align: center;
}

.time {
    flex: 1;
    margin-left: 20px;
}

.slide {
    flex: 4;
    margin: 0 20px;
}

.transition {
    flex: 2;
}

.menuBar {
    width: 25px;
    height: 2px;
    background-color: black;
    margin: 6px 0;
}
</style>
