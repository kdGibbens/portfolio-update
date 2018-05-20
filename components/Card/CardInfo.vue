<template>
    <div class="info-card">

        <div class="card-header">
            <img src="~/assets/images/kelly-gibbens.jpg" alt="Kelly Gibbens - Front-end Web Developer" class="card-img">
        </div>

        <div class="card-body">
            <h2 class="name">
                {{name}}
            </h2>
            <p class="job-title">
                {{job}}
            </p>
            <p class="email">
                <a :href="email">{{emailText}}</a>
            </p>
            
        </div>

        <div class="card-footer">
            <a v-for="icon in icons" v-bind:key="icon.company" :href="icon.url"><font-awesome-icon :icon="[icon.fa, icon.company]" class="icon" /></a>
        </div>

    </div>
</template>

<script>
export default {
    name: 'card-info',
    data(){
        return {
            name: 'Kelly Gibbens',
            job: 'Front-end Developer',
            email: 'mailto:gibbenskd@gmail.com',
            emailText: 'gibbenskd@gmail.com',
            icons: {
                github: {
                    fa: 'fab',
                    company: 'github',
                    url: 'https://github.com/kdGibbens'
                },
                linkedin: {
                    fa: 'fab',
                    company: 'linkedin',
                    url: 'https://www.linkedin.com/in/kelly-gibbens-0987a039/'
                }
            }
        }
    }
}
</script>
<style>

</style>

