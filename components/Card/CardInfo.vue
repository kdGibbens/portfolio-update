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
    .info-card {
        background: white;
        padding: 1rem;
        border-radius: 5px;
        box-shadow: 0 0 10px 0 rgba(0,0,0,0.5);
        background: linear-gradient(#546d8c 0%,#ba555f 100%);
    }

    .info-card .card-header {
        background: url(~/assets/images/kelly-gibbens.jpg) no-repeat;
        height: 15rem;
        width: 15rem;
        background-size: cover;
        position: relative;
        background-position: top;
        border-radius: 50%;
        border: 6px solid rgb(31, 89, 155);
        box-shadow: 0 0 10px 3px rgba(0,0,0,0.5)
    }
    .card-body {
        padding: 1rem;
        position: relative;
        text-align: center;
       
    }
    .card-body h2, .card-body p {
        color: #fffff0;
    }
    .card-body a {
        color: #fffff0;
        text-decoration: none;
        transition: 1s;
    }
    .card-body a:hover {
        text-decoration: underline;
    }
    .card-footer {
        display: grid;
        grid-template-columns: repeat(2,1fr);
        justify-items: center;
    }
    .card-footer svg {
        font-size: 2rem;
        color: #fffff0;
        transition: .5s;
        cursor: pointer;
    }
    .card-footer svg:hover {
        color: #546d8c;
    }
</style>

