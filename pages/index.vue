<template>
    <Header />

    <div class="body">

        <div class="left">
            <img class="profile-img" src="assets/profile.png">

            <p class="email">Contact: fitria.zusni06@gmail.com</p>
            <div class="social-media">
                <img class="linkedin-icon" src="assets/icon_linkedin.png">
                <img class="github-icon" src="assets/icon_github.png">
                <img class="medium-icon" src="assets/icon_medium.png">
            </div>
        </div>
        <div class="right">
            <div class="right-content">
                <h1>Fitria Zusni Farida</h1>
                <p>(she/her)</p>

                <p>Hi there! 👋</p>
                <p>I'm a final-year student majoring in <span class="pink">Computer Science and Engineering at Southern University of Science and Technology (SUSTech / 南方科技大学)</span>, China. </p>
                <p>Currently, my interests lie at the intersection of technology, data, and design. </p>
                <p>Specificaly:</p>
                <p>
                    <ul>
                        <li>turning data into actionable insights and building machine learning models</li>
                        <li>solving problems through user-centered design to create usable and intuitive experiences</li>
                        <li>building deliverable software systems and exploring software engineering concepts.</li>
                    </ul>
                </p>
                <p>I am expected to graduate with my bachelor’s degree in June 2025, and <b>I’m actively seeking internship or full-time opportunities as Data Analyst, Data Scientist, or AI/Software Engineer!</b> 🚀</p>
            </div>

        </div>

    </div>

</template>
<script>
import Header from '@/components/Header.vue'
// import { HeroIcon } from '@heroicons/vue';

</script>
<style>

html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    justify-content: center;
    align-items: center;
}

.body {
    margin: 32px 180px;
    padding: 48px 18px;
    height: 500px;
    width: 1080px;
    border: 1px solid #ccc;
    display: flex;
    justify-content: space-between;
    border-radius: 5px;
}

.right h1 {
    font-size: 36px;
}

.left {
    width: 30%;
    justify-content: center;
    align-items: center;
    text-align: center;
    margin-top: 20px;
}

.right {
    width: 65%;
}
.right-content {
    padding-right: 30px;
}

.left img {
    width: 210px;
    height: 210px;
    object-fit: cover;
    border-radius: 50%;
    filter: brightness(1.2);
}

.social-media {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
}

.social-media img {
    width: 42px;
    height: 42px;
    object-fit: cover;
}
.social-media img:hover{
    cursor: pointer;
}
.pink {
    color: #e43b63;
}
.pink:hover{
    cursor: pointer;
    text-decoration: underline;
    color: #c32f52;
}
.email:hover{
    cursor: pointer;
    text-decoration: underline;
}

</style>