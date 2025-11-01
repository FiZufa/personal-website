<template>
    <Header />

    <div class="body">

        <div class="left">
            <img class="profile-img" src="assets/profile.png">

            <p class="email">Email: fitria.zusni06@gmail.com</p>
            <div class="social-media">
                
                <a href="https://linkedin.com/in/fitria-zusni-farida" target="_blank" rel="noopener noreferrer">
                    <img class="linkedin-icon" src="assets/icon_linkedin.png" alt="linkedin icon">
                </a> 
                <a href="https://github.com/FiZufa" target="_blank" rel="noopener noreferrer">
                    <img class="github-icon" src="assets/icon_github.png" alt="GitHub Icon">
                </a>
                <a href="https://medium.com/@fi.zufa0612" target="_blank" rel="noopener noreferrer">
                    <img class="medium-icon" src="assets/icon_medium.png" alt="medium icon">
                </a>               
                <!-- <a href="https://id.pinterest.com/" target="_blank" rel="noopener noreferrer">
                    <img class="pinterest-icon" src="assets/icon_pinterest.png" alt="pinterest icon">
                </a>       -->
            </div>
        </div>
        <div class="right">
            <div class="right-content">
                <div class="my-name">
                    <h1 style="margin-bottom: 1px;">Fitria Zusni Farida</h1>
                    <p style="margin-top: 0;">(she/her)</p>
                </div>

                <p>Hi there! 👋</p>
                <p>I'm a graduate with a degree in Computer Science and Engineering from <a class="pink" href="https://www.sustech.edu.cn/" target="_blank" rel="noopener noreferrer">Southern University of Science and Technology (SUSTech / 南方科技大学)</a>, China. </p>
                <p>I am deeply interested in Data Science and Natural Language Processing (NLP).</p>
                <p>Currently, I am a Machine Learning & NLP Engineer intern at Purple Box AI, focusing on NLP, LLMs, and Retrieval Augmented Generation (RAG).</p>
                <p>I have gained several hands-on experiences from course and group projects in AI, data, software development, and UI/UX. Feel free to explore my portfolio page ✨</p>
                <!-- <p>I am expected to graduate with my bachelor’s degree in June 2025, and I’m actively seeking internship or full-time opportunities to share my ideas and contribute to meaningful projects! 🚀</p> -->
            </div>

        </div>

    </div>

    <div class="divider"></div>

    <div class="about-me" id="about-me">
        <h1>About me 🍃</h1>
        <div>
            <p>I live in Nganjuk, East Java, Indonesia. I also had been living in Shenzhen, China, for over two years to pursue my undergraduate studies🎓.</p>
            <p>My hobbies are reading, writing, cooking, running, biking, flexibility training (a.k.a. yoga), picnic, and listening to musics. I like reading books related to psychology and philosophy. I'm highly passionate learning psychology and cognitive science as well! 👤🧠 </p>
            <p>I speak Indonesian (Bahasa) as my native language and use English at workplace. I also learn Chinese as my third language!😊</p>
            <p>Feel free to explore my social media or connect with me! ✨</p>
        </div>

    </div>


    <Footer />

</template>
<script>
import Header from '@/components/Header.vue';
// import { HeroIcon } from '@heroicons/vue';
import Divider from '@/components/Divider.vue';
import { Footer } from '#components';
import VueMq from 'vue-mq';

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
    padding: 48px 0;
    height: auto;
    border: 1px solid #ccc;
    display: flex;
    justify-content: space-between;
    border-radius: 5px;
    flex-wrap: wrap;
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

.my-name {
    border-bottom: #ccc 0.5px solid;
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
    text-decoration: none;
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
.about-me{
    margin: 0 180px;
    flex-wrap: wrap;
}

.divider {
    border-top: 1px #ccc solid;
    margin: 64px 180px;
    align-items: center;
    text-align: center;
    justify-content: center;
}

@media screen and (min-width: 1599px) {
    .body {
        width: 1200px;  /* Increase width for larger screens */
        margin: 32px auto;  /* Center the body content */
        padding: 48px 0;
    }

    .left {
        width: 25%; /* Adjust width of the left side for more space on large screens */
    }

    .right {
        width: 70%;  /* Adjust width of the right side */
    }

    .right-content {
        padding-right: 5%;  /* Adjust padding for larger screens */
    }

    .my-name h1 {
        font-size: 48px;  /* Increase font size for large screens */
    }

    .right-content p, .right-content li, .about-me p {
        font-size: 18px;  /* Increase font size for better readability */
    }

    .email {
        font-size: 16px;  /* Increase font size */
    }

    .social-media img {
        width: 48px;
        height: 48px;
    }

    .divider {
        margin: 64px 180px;
    }
}


/* Mobile and Tablet Styles */
@media screen and (max-width: 1024px) {

    .body {
        margin: 16px 3%;
        flex-direction: column; /* Stacks content vertically on smaller screens */
    }

    .left {
        width: 100%; /* Stacks the left and right content to 100% width */
        text-align: center; /* Centers text for mobile screens */
        margin: 10px 0;
    }
    .right {
        width: 100%;
        margin: 5% 5%;
    }

    .left img {
        width: 15rem;  /* Makes image 50% of the container's width */
        height: 15rem; /* Makes height equal to width */
    }
    

    .social-media img {
        width: 3rem;
        height: 3rem;
    }

    .right-content {
        padding-right: 10%;
    }

    .my-name h1, .about-me h1 {
        font-size: 42px;
    }

    .right-content p, .right-content li, .about-me p {
        font-size: 16px;
    }

    .email {
        font-size: 14px;
    }

    .about-me {
        margin: 0 5%;
    }

    .divider {
        margin: 3% 3%;
        align-items: center;
        text-align: center;
        justify-content: center;
    }
}



</style>
