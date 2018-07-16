<template>
    <div class="works" id="works">
        <div v-for="experience in experiences" class="work-container" :key="experience.id">
            <div class="work">
                <div class="position">
                    <h1>{{experience.position}}</h1>
                </div>
                <div class="company">
                    <h3>{{experience.company}}</h3>
                </div>
                <div class="date">
                    {{experience.from}} — {{experience.to}}
                </div>
                <div class="description">
                    {{experience.description}}
                </div>
                <div class="technologies">
                    <div class="technology" v-for="technology in experience.technologies" :key="technology.id">
                        <div v-bind:class="[technology.tag]">
                            <p>{{technology.tech}}</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'workExperience',
        data() {
            return {
                experiences: [
                    {
                        id: 1,
                        company: 'DibzTech, Inc.',
                        type: 'Full-time',
                        position: 'Associate Software Engineer',
                        from: 'February, 2018',
                        to: 'Present',
                        description: '',
                        technologies: [
                            {
                                id: 1,
                                tech: 'PHP',
                                tag: 'primary'
                            },
                            {
                                id: 2,
                                tech: 'Laravel',
                                tag: 'primary'
                            },
                            {
                                id: 3,
                                tech: 'MySQL',
                                tag: 'primary'
                            },
                            {
                                id: 4,
                                tech: 'RESTFul API',
                                tag: 'primary'
                            },
                            {
                                id: 5,
                                tech: 'Postman',
                                tag: 'secondary'
                            },
                            {
                                id: 6,
                                tech: 'Amazon AWS',
                                tag: 'secondary'
                            },
                            {
                                id: 7,
                                tech: 'Pusher',
                                tag: 'secondary'
                            },
                            {
                                id: 8,
                                tech: 'Mail',
                                tag: 'secondary'
                            },
                            {
                                id: 9,
                                tech: 'SMS (Promotexter)',
                                tag: 'secondary'
                            },
                            {
                                id: 10,
                                tech: 'PHP Excel',
                                tag: 'secondary'
                            },
                            {
                                id: 11,
                                tech: 'GIT',
                                tag: 'primary'
                            },
                        ]
                    },
                    {
                        id: 2,
                        company: 'Mellow Yellow Sunset Cruise',
                        type: 'Freelance',
                        position: 'Web Developer',
                        from: 'September, 2017',
                        to: 'February, 2018',
                        description: '',
                        technologies: [
                            {
                                id: 1,
                                tech: 'PHP',
                                tag: 'primary'
                            },
                            {
                                id: 2,
                                tech: 'Laravel',
                                tag: 'primary'
                            },
                            {
                                id: 3,
                                tech: 'MySQL',
                                tag: 'primary'
                            },
                            {
                                id: 4,
                                tech: 'Foundation CSS',
                                tag: 'primary'
                            },
                            {
                                id: 5,
                                tech: 'JQuery & Ajax',
                                tag: 'primary'
                            },
                            {
                                id: 6,
                                tech: 'HTML5',
                                tag: 'primary'
                            },
                            {
                                id: 7,
                                tech: 'PHP Excel',
                                tag: 'secondary'
                            },
                        ]
                    },
                    {
                        id: 3,
                        company: 'Gaia South, Inc.',
                        type: 'Freelance',
                        position: 'Database Administrator',
                        from: 'July, 2017',
                        to: 'October, 2017',
                        description: '',
                        technologies: [
                            {
                                id: 1,
                                tech: 'PHP',
                                tag: 'primary'
                            },
                            {
                                id: 2,
                                tech: 'HTML5',
                                tag: 'primary'
                            },
                            {
                                id: 3,
                                tech: 'JQuery & Ajax',
                                tag: 'primary'
                            },
                            {
                                id: 4,
                                tech: 'PHP Excel',
                                tag: 'secondary'
                            },
                            {
                                id: 5,
                                tech: 'MySQL',
                                tag: 'primary'
                            },
                        ]
                    },
                    {
                        id: 4,
                        company: 'Simplex Internet, Inc.',
                        type: 'Full-time',
                        position: 'PHP Developer',
                        from: 'October, 2016',
                        to: 'February, 2017',
                        description: '',
                        technologies: [
                            {
                                id: 1,
                                tech: 'PHP',
                                tag: 'primary'
                            },
                            {
                                id: 2,
                                tech: '12R (In-house PHP Framework)',
                                tag: 'primary'
                            },
                            {
                                id: 3,
                                tech: 'CStore (In-house PHP E-Commerce Framework)',
                                tag: 'primary'
                            },
                            {
                                id: 4,
                                tech: 'MySQL',
                                tag: 'primary'
                            },
                            {
                                id: 5,
                                tech: 'Redis',
                                tag: 'primary'
                            },
                            {
                                id: 6,
                                tech: 'JQuery & Ajax',
                                tag: 'primary'
                            },
                            {
                                id: 7,
                                tech: 'SUIO (In-house CSS Framework)',
                                tag: 'primary'
                            },
                            {
                                id: 8,
                                tech: 'Git & Mercurial',
                                tag: 'primary'
                            },
                            {
                                id: 9,
                                tech: 'Jenkins',
                                tag: 'secondary'
                            },
                            {
                                id: 10,
                                tech: 'JIRA',
                                tag: 'secondary'
                            },
                            {
                                id: 11,
                                tech: 'Confluence',
                                tag: 'secondary'
                            },
                            {
                                id: 12,
                                tech: 'Web Sockets',
                                tag: 'secondary'
                            },
                        ]
                    },
                    {
                        id: 5,
                        company: 'Drake Marketing and Equipment Corporation',
                        type: 'Freelance',
                        position: 'VB .NET Developer',
                        from: 'March, 2014',
                        to: 'April, 2014',
                        description: '',
                        technologies: [
                            {
                                id: 1,
                                tech: 'Visual Basic .NET',
                                tag: 'primary'
                            },
                            {
                                id: 2,
                                tech: 'SQLite',
                                tag: 'primary'
                            },
                        ]
                    },
                    {
                        id: 6,
                        company: 'Various clients for smaller projects',
                        type: 'Freelance',
                        position: 'Freelance Programmer',
                        from: 'October, 2012',
                        to: 'Present',
                        description: '',
                        technologies: [
                            {
                                id: 1,
                                tech: 'PHP',
                                tag: 'primary'
                            },
                            {
                                id: 2,
                                tech: 'Javascript',
                                tag: 'primary'
                            },
                            {
                                id: 3,
                                tech: 'Laravel',
                                tag: 'primary'
                            },
                            {
                                id: 4,
                                tech: 'Code Igniter',
                                tag: 'primary'
                            },
                            {
                                id: 5,
                                tech: 'JQuery & Ajax',
                                tag: 'primary'
                            },
                            {
                                id: 6,
                                tech: 'HTML5',
                                tag: 'primary'
                            },
                            {
                                id: 7,
                                tech: 'Bootstrap CSS',
                                tag: 'primary'
                            },
                            {
                                id: 8,
                                tech: 'Foundation CSS',
                                tag: 'primary'
                            },
                            {
                                id: 9,
                                tech: 'VueJS',
                                tag: 'primary'
                            },
                            {
                                id: 10,
                                tech: 'React Native',
                                tag: 'primary'
                            },
                            {
                                id: 11,
                                tech: 'Android Native Development',
                                tag: 'primary'
                            },
                            {
                                id: 12,
                                tech: 'PHP Excel',
                                tag: 'secondary'
                            },
                        ]
                    }
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import '../assets/scss/work.scss'
</style>
