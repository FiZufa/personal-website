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
                <a href="https://id.pinterest.com/" target="_blank" rel="noopener noreferrer">
                    <img class="pinterest-icon" src="assets/icon_pinterest.png" alt="pinterest icon">
                </a>      
            </div>
        </div>
        <div class="right">
            <div class="right-content">
                <div class="my-name">
                    <h1 style="margin-bottom: 1px;">Fitria Zusni Farida</h1>
                    <p style="margin-top: 0;">(she/her)</p>
                </div>

                <p>Hello world! 👋</p>
                <p>I'm a final-year student majoring in <a class="pink" href="https://www.sustech.edu.cn/" target="_blank" rel="noopener noreferrer">Computer Science and Engineering at Southern University of Science and Technology (SUSTech / 南方科技大学)</a>, China. </p>
                <p>Currently, my interests lie at the intersection of <b>technology, data,</b> and <b>design</b>.</p>
                <p>Specifically:</p>
                <p>
                    <ul>
                        <li>turning data into actionable insights and building machine learning models</li>
                        <li>solving problems through user-centered design to create intuitive experiences</li>
                        <li>building deliverable software systems and exploring software engineering concepts.</li>
                    </ul>
                </p>
                <p>I am expected to graduate with my bachelor’s degree in June 2025, and <b>I’m actively seeking internship or full-time opportunities as Data Analyst, Data Scientist, or AI/Software Engineer!</b> 🚀</p>
            </div>

        </div>

    </div>

    <div class="divider"></div>

    <div class="about-me" id="about-me">
        <h1>About me 🍃</h1>
        <div>
            <p>I grew up in Nganjuk, East Java, Indonesia, and have been living in Shenzhen, China, for over two years to pursue my undergraduate studies🎓.</p>
            <p>Apart from my study, I enjoy learning new things, especially in areas such as psychology 👤, neurobiology 🧠, children development 👨‍👩‍👧‍👦, health 💪, and nutrition 🍒.</p>
            <p>My hobbies are reading, cooking, running, biking, flexibility training (a.k.a. yoga), and listening to musics. I like reading novels and books related to psychology and neurobiology 📖.  I am not a competitive runner, but I enjoy 2k meters running every morning while listening to musics 🏃‍♀️🎶🌞. I like to cook my home dishes, especially Indonesian food! Let me know if you have an interesting recipe—I’d love to learn it! 🍳😋</p>
            <p>I speak Indonesian (Bahasa) as my native language and use English on a daily basis. Furthermore, I also learn Chinese as my third language!😊</p>
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
    width: 1080px;
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
    
}

.divider {
    border-top: 1px #ccc solid;
    margin: 64px 180px;
    align-items: center;
    text-align: center;
    justify-content: center;
}

/* Mobile and Tablet Styles */
@media screen and (max-width: 1024px) {
    .body {
        margin: 16px 64px;
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
        width: 250px; /* Makes image smaller on mobile */
        height: 250px;
    }

    .social-media img {
        width: 48px;
        height: 48px;
    }

    .right h1 {
        font-size: 28px; /* Smaller font size for mobile */
    }

    .right-content {
        padding-right: 10%; 
    }

    .right-content h1 {
        font-size: 48px;
    }

    .about-me {
        margin: 0 64px;
    }

    .divider {
        margin: 64px 64px;
        align-items: center;
        text-align: center;
        justify-content: center;
    }
}

@media screen and (max-width: 600px) {
    .body {
        margin: 16px; /* Smaller margin for very small screens */
    }

    .left img {
        width: 250px; /* Even smaller profile image */
        height: 250px;
    }

    .social-media img {
        width: 30px; /* Smaller icons */
        height: 30px;
    }

    .right h1 {
        font-size: 24px; /* Even smaller title for small screens */
    }

    .right-content {
        font-size: 14px; /* Adjust font size for readability on small screens */
    }

    .about-me {
        margin: 0 16px; /* Reduce margin for small screens */
    }

    .divider {
        margin: 64px 16px; /* Adjust divider margin for mobile */
    }
}
</style>