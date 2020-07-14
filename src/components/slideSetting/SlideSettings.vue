<template>
    <div id="SequenceSettings" class="column">
        <draggable v-model="sequence.slides" ghost-class="ghost">
            <transition-group type="transition" name="flip-list">
                <SingleSlideSetting
                    v-for="slide in sequence.slides"
                    :key="slide.id"
                    :slideData="slide"
                />
            </transition-group>
        </draggable>
        <div @drop.prevent="drop" @dragover.prevent class="drop">
            drop
        </div>
    </div>
</template>

<script>
/* eslint-disable */
import SingleSlideSetting from './SingleSlideSetting.vue';
import draggable from 'vuedraggable';

export default {
    props: {
        sequence: Object
    },
    components: {
        SingleSlideSetting,
        draggable
    },
    methods: {
        drop(e) {
            const slide = JSON.parse(e.dataTransfer.getData('slide'));
            this.sequence.slides.push({
                id: slide.id,
                slide: slide.slide,
                duration: 0,
                transitionToNext: 'cut'
            });
        }
    }
};
</script>

<style scoped>
#SequenceSettings {
    flex: 4;
}

.sortable-drag {
    opacity: 0;
}

.ghost {
    background-color: grey;
}

.flip-list-move {
    transition: transform 0.5s;
}

.column {
    display: flex;
    flex-direction: column;
}

.drop {
    display: flex;
    justify-content: center;
    align-items: center;
    border: 1px dashed black;
    height: 40px;
    border-radius: 5px;
}

#SequenceSettings .thing-drag {
    opacity: 0;
}
</style>
