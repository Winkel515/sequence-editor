<template>
    <div id="app">
        <div class="row">
            <SlideSettings :sequence="sequence" />
            <SlideSelect :availableSlides="availableSlides" />
        </div>
    </div>
</template>

<script>
import SlideSettings from './components/slideSetting/SlideSettings.vue';
import SlideSelect from './components/slideSelect/SlideSelect.vue';

export default {
    data() {
        return {
            sequence: {
                slides: [
                    {
                        id: 'rhoerjher-herhoerh',
                        slide: 'Slide 1',
                        duration: 3,
                        transitionToNext: 'cut'
                    },
                    {
                        id: 'gegerg-35832g4g',
                        slide: 'Slide 2',
                        duration: 4,
                        transitionToNext: 'cut'
                    },
                    {
                        id: 'nreogrg-353fnev',
                        slide: 'Slide 1',
                        duration: 2,
                        transitionToNext: 'cut'
                    },
                    {
                        id: 'goeg-3g3hdk',
                        slide: 'Slide 4',
                        duration: 7,
                        transitionToNext: 'cut'
                    }
                ]
            },
            availableSlides: [
                {
                    id: '309t3ug34g',
                    slide: 'Slide 1'
                },
                {
                    id: '4t943gj4334g',
                    slide: 'Slide 2'
                },
                {
                    id: '3498gh43gn43og',
                    slide: 'Slide 3'
                },
                {
                    id: 'rgu3hg834g4n',
                    slide: 'Slide 4'
                },
                {
                    id: 'g3oigh3443',
                    slide: 'Slide 5'
                },
                {
                    id: 'r39g43hgrg',
                    slide: 'Slide 6'
                }
            ]
        };
    },
    components: { SlideSettings, SlideSelect }
};
</script>

<style>
.row {
    display: flex;
    width: 100%;
}
</style>
