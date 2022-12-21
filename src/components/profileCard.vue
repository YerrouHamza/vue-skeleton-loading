<script>

    import {ref} from 'vue';

    const loadDataUser = async () => {
        return new Promise((resolve) => {
            setTimeout(() => {
                resolve({
                    name: 'Hamza Yerrou',
                    pic: 'https://i.postimg.cc/xCh7sBpg/cool-neon-blue-profile-picture-u9y9ydo971k9mdcf.jpg',
                    description: "I'm a Front-End Web Developer and I always like to search more about Front-End skills"
                })
            }, 4000);
        })
    }


    export default {
        async setup () {
            const userData = ref(await loadDataUser())

            return {
                userData
            } 
        }
    }
</script>


<template>
    <div class="profile-card">
        <div class="profile-img">
            <img :src="userData.pic" />
        </div>
        <div class="profile-info">
            <span> Written By </span>
            <h2>{{ userData.name }}</h2>
            <p>{{ userData.description }}</p>
        </div>
    </div>

</template>


<style>
    .profile-card {
        width: 100%;
        max-width: 700px;
        min-height: 120px;
        background-color: rgb(55, 55, 55);
        padding: 20px 30px;
        border-radius: 10px;
        margin: 30px auto;
        overflow: hidden;
    }

    .profile-img {
        width: 13%;
        float: left;
    }
    .profile-img img {
        width: 100%;
        height: auto;
        border-radius: 50%;
        padding: 3px;
        border: 3px solid var(--green);
    }
    
    .profile-info {
        width: 85%;
        float: right;
    }
    .profile-info span {
        letter-spacing: 3px;
        text-transform: uppercase;
        color: rgb(148, 148, 148);
        font-size: .8rem;
    }
    .profile-info h2 {
        font-size: 1.5rem;
        color: #fff;
        margin: 5px 0 10px 0;
        line-height: 1;
    }
    .profile-info p {
        line-height: 1.4;
        color: #cfcfcf;
    }
</style>