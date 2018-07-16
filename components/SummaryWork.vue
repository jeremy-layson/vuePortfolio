<template>
    <div class="summary-work" id="summary-work">
        <div class="card-collection" v-for="cardsets in sets" :key="cardsets.id">
            <div class="card" 
                v-bind:class="[cardsets.floatDirection]" 
                v-for="card in cardsets.cardSet" :key="card.id">
                <div class="card-content" v-bind:class="[card.color]">
                    <p>{{card.cardText}}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import $ from 'JQuery'
    export default {
        name: 'summaryWork',
        data() {
            return {
                sets: [
                    {
                        id: 1,
                        floatDirection: 'float-left',
                        cardSet: [
                            {
                                id: 1,
                                cardText: 'I am a developer. This is my story. As an enthusiast, as a lifelong student and as a professional.',
                                color: 'color-1',
                            },
                            {
                                id: 2,
                                cardText: 'February of 2018 when I started working with Dibz. It is an amazing company that solves the parking problem with the help of mobile application.',
                                color: 'color-2',
                            },
                            {
                                id: 3,
                                cardText: 'I am one of the two back-end developer of the company. I mostly worked on maintaining its main product; making sure it works as intended.',
                                color: 'color-3',
                            },
                            {
                                id: 4,
                                cardText: 'On top of that, I also implement new features, reproduce and fix bugs and participate in dev meetings for planning and tackling issues.',
                                color: 'color-4',
                            },
                            {
                                id: 5,
                                cardText: 'I\'ve learned lots of things here. Maintainable and readable code. Scaling the system. Prioritization of tasks and switching from one task to another.',
                                color: 'color-5',
                            }

                        ]
                    },
                    {
                        id: 2,
                        floatDirection: 'float-right',
                        cardSet: [
                            {
                                id: 1,
                                cardText: 'I am a developer. This is my story. As an enthusiast, as a lifelong student and as a professional.',
                                color: 'color-6',
                            },
                            {
                                id: 2,
                                cardText: 'February of 2018 when I started working with Dibz. It is an amazing company that solves the parking problem with the help of mobile application.',
                                color: 'color-7',
                            },
                            {
                                id: 3,
                                cardText: 'I am one of the two back-end developer of the company. I mostly worked on maintaining its main product; making sure it works as intended.',
                                color: 'color-8',
                            },
                            {
                                id: 4,
                                cardText: 'On top of that, I also implement new features, reproduce and fix bugs and participate in dev meetings for planning and tackling issues.',
                                color: 'color-9',
                            },
                            {
                                id: 5,
                                cardText: 'I\'ve learned lots of things here. Maintainable and readable code. Scaling the system. Prioritization of tasks and switching from one task to another.',
                                color: 'color-10',
                            }

                        ]
                    },
                    {
                        id: 3,
                        floatDirection: 'float-left',
                        cardSet: [
                            {
                                id: 1,
                                cardText: 'I am a developer. This is my story. As an enthusiast, as a lifelong student and as a professional.',
                                color: 'color-11',
                            },
                            {
                                id: 2,
                                cardText: 'February of 2018 when I started working with Dibz. It is an amazing company that solves the parking problem with the help of mobile application.',
                                color: 'color-12',
                            },
                            {
                                id: 3,
                                cardText: 'I am one of the two back-end developer of the company. I mostly worked on maintaining its main product; making sure it works as intended.',
                                color: 'color-13',
                            },
                            {
                                id: 4,
                                cardText: 'On top of that, I also implement new features, reproduce and fix bugs and participate in dev meetings for planning and tackling issues.',
                                color: 'color-14',
                            },
                            {
                                id: 5,
                                cardText: 'I\'ve learned lots of things here. Maintainable and readable code. Scaling the system. Prioritization of tasks and switching from one task to another.',
                                color: 'color-15',
                            }

                        ]
                    },
                ]
            }
        },
        
    }
</script>

<style lang="scss" scoped>
    @import '../assets/scss/summary.scss'
</style>
