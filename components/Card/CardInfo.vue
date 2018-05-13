<template>
    <div class="info-card">

        <div class="card-header">
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
            <font-awesome-icon :icon="[icon.fa, icon.company]" class="icon" v-for="icon in icons" v-bind:key="icon.company" :alt="icon.company"/>
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
                    company: 'github'
                },
                linkedin: {
                    fa: 'fab',
                    company: 'linkedin'
                }
            }
        }
    }
}
</script>
<style>
    .info-card {
        background: white;
        padding: 1rem;
        border-radius: 5px;
    }

    .info-card .card-header {
        background: url(~/assets/images/kelly-gibbens.jpg) no-repeat;
        height: 15rem;
        width: 15rem;
        background-size: cover;
        position: relative;
        background-position: top;
        border-radius: 5px;
    }
    .card-header:after {
        content: '';
        position: absolute;
        width: 100%;
        height: 100%;
        background: linear-gradient(135deg, #5397cc 0%,#ba555f 100%);
        opacity: .35;
    }
    .card-body {
        padding: 2rem 1rem 1rem;
        position: relative;
    }
    .card-body::before {
        content: '';
        position: absolute;
        background: white;
        height: 4rem;
        top: -1rem;
        left: 0;
        width: 100%;
        transform: skewX(-10deg);
        z-index: 1;
    }
</style>

