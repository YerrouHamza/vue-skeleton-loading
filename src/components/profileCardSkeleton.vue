<script>
</script>


<template>
    <div class="profile-card">
        <div class="profile-img">
            <img />
        </div>
        <div class="profile-info">
            <span />
            <h2 />
            <p />
        </div>
    </div>

</template>


<style scoped>
    .profile-img img {
        width: 100%;
        padding-top: 100%;
        animation: background-flash 1.9s infinite;
        border: none;
    }
    
    .profile-info span {
        display: block;
        width: 30%;
        height: 15px;
        animation: background-flash 1.9s infinite;
    }
    .profile-info h2 {
        width: 300px;
        height: 25px;
        animation: background-flash 1.9s infinite;
    }
    .profile-info p {
        width: 90%;
        height: 40px;
        animation: background-flash 1.9s infinite;
    }


    @keyframes background-flash {
        0% {
            background-color: #888;
        }
        50% {
            background-color: #c4c4c4;
        }
        100% {
            background-color: #888;
        }
    }
</style>