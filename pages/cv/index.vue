<template>
    <Header />

    <div class="cv-body">
        <div class="section">
            <h1 class="sub-title">Bio</h1>
            <p>A final-year Computer Science and Engineering student at Southern University of Science and Technology (SUSTech), China, with keen interests in Human-centered Artificial Intelligence (HAI) and Human-Computer Interaction (HCI). Specifically, I am interested in understanding human behavior (psychologically and linguistically) through NLP and HCI methods.</p>
        </div>

        <Line />

        <div class="section">
            <h1 class="sub-title">Skills</h1>
            <ul>
                <li v-for="(value, key) in data.dataSkills" :key="key">
                  <span class="bold">{{ key }}</span>: {{ value }}
                </li>
            </ul>
              
        </div>

        <Line />

        <div class="section-edu">
            <h1 class="sub-title">Education</h1>
            <a style="text-decoration: none;" href="https://www.sustech.edu.cn/" target="_blank" rel="noopener noreferrer"><p class="pink">Southern University of Science and Technology (SUSTech / 南方科技大学)</p></a>
            <p><span class="bold">Bachelor</span>, Department of Computer Science and Engineering</p>
            <p>September 2021 - June 2025 (Expected graduation) </p>
            <p>Relevant courseworks: Data Structures and Algorithm, Algorithm Design and Analysis, Introduction to Mathematical Logic, Artificial Intelligence, C/C++ Programming Design, Computer Networks, Operating Systems, Object-oriented Analysis and Design, Computer System Design, Discrete Mathematics, Probability and Statistics, Principle of Database Systems, Software Engineering, Machine Learning, Deep Learning, Natural Language Processing</p>
            
        </div>

        <Line />

        <div class="section">
            <h1 class="sub-title">Experience</h1>
            <div v-for="(training, index) in data.experience" :key="index" class="experience">
                <!-- <p class="bold">{{ training.name }}</p> -->
                <p class="title-name">{{ training.name }}</p>
                <p>{{ training.time }}</p>
                <ul>
                    <li v-for="(desc, descIndex) in training.desc" :key="descIndex"> {{ desc }}</li>
                </ul>
                <div class="cred-btn"><a class="cred-link" :href="training.link" target="_blank" rel="noopener noreferrer">View credential</a><img src="/assets/view-btn.png" style="height: 12px;"></div>
            </div>
        </div>

        <Line />

        <div class="section">
            <h1 class="sub-title">Awards</h1>
            <div v-for="(award, index) in data.awards" :key="index" class="award">
                <p class="bold">{{ award.name }}</p>
                <p style="font-style: italic;">{{ award.issuer }}</p>
                <p>{{ award.time }}</p>
                <ul>
                    <li v-for="(desc, descIndex) in award.desc" :key="descIndex">{{ desc }}</li>
                </ul>
            </div>

        </div>

        <Line />

        <div class="section">
            <h1 class="sub-title">Training</h1>
            <div v-for="(training, index) in data.trainings" :key="index" class="training">
                <!-- <p class="bold">{{ training.name }}</p> -->
                <p class="title-name">{{ training.name }}</p>
                <p>{{ training.time }}</p>
                <ul>
                    <li v-for="(desc, descIndex) in training.desc" :key="descIndex">{{ desc }}</li>
                </ul>
                <div class="cred-btn"><a class="cred-link" :href="training.link" target="_blank" rel="noopener noreferrer">View credential</a><img src="/assets/view-btn.png" style="height: 12px;"></div>
            </div>
        </div>

        <Line />

        <div class="section">
            <h1 class="sub-title">Activities</h1>
            <div v-for="(act, index) in data.activities" :key="index" class="activity">
                <p><span class="bold">{{ act.role }}</span>, {{ act.name }}</p>
                <p style="font-style: italic;">{{ act.issuer }}</p>
                <p>{{ act.where }}</p>
                <ul>
                    <li v-for="(desc, descIndex) in act.desc" :key="descIndex">{{ desc }}</li>
                </ul>
            </div>
        </div>

        <Line />

        <div class="section">
            <h1 class="sub-title">Certifications</h1>
            <div v-for="(certif, index) in data.certifications" :key="index" class="certif">
                <p class="title-name">{{ certif.name }}</p>
                <p>{{ certif.when }}</p>
                <p>Skills: 
                    <span v-for="(skill, skillIndex) in certif.skills" :key="skillIndex">
                      {{ skill }},
                    </span>
                </p>
                <div class="cred-btn"><a class="cred-link" :href="certif.link" target="_blank" rel="noopener noreferrer">View credential</a><img src="/assets/view-btn.png" style="height: 12px;"></div>
            </div>
        </div>
        
    
    </div>

    <Footer />

</template>
<script>
import Header from '@/components/Header.vue';
import dataSkills from '@/data/data_skills.json';
import awards from '@/data/data_awards.json';
import trainings from '@/data/data_training.json';
import activities from '@/data/data_activities.json';
import certifications from '@/data/data_certification.json';
import experience from '@/data/experience.json';

import Line from '~/components/Line.vue';
import { Footer } from '#components';

export default {
  data() {
    return {
      data: {
        dataSkills,
        experience,
        awards,
        trainings,
        activities,
        certifications
      },
    };
  },
};

</script>
<style>

html, body {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;

}

.cv-body{
    margin: 32px 180px;
}

.sub-title {
    font-weight: 500;
}

.bold {
    font-weight: 650;
}

.experience p, .award p, .training p, .activity p, .certif p, .section-edu p {
    margin: 4px 0; /* Adjust the value as needed */
}

.experience, .award, .training, .activity, .certif {
    margin-top: 4px;
    margin-bottom: 16px;
}

.pink, .certif .bold, .training .bold {
    color: #e43b63;
}

.pink:hover, .certif .bold:hover, .training .bold:hover {
    cursor: pointer;
    text-decoration: underline;
    color: #c32f52;
}

.cred-btn {
    display: inline;
    padding: 4px 8px;
}

.cred-btn:hover {
    color: #c32f52;
    text-decoration: underline;
}

.cred-link {
    color: #c32f52;
    text-decoration: none;
    cursor: pointer;
}

.skill {
    background-color: #ccc;
    border-radius: 2px;
    padding: 1px 8px;
    margin: 2px 2px;
    font-size: 12px;
}

.title-name {
    font-weight: 650;
}

@media screen and (max-width: 1024px) {
    .cv-body {
        margin: 0 3%;
    }
}

</style>