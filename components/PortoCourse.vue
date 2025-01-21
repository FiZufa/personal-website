<template>
    <h2>🎓Relavant Undergraduate Coursework Projects</h2>

    <div class="porto-section">
        
        <div class="projects">
            <p>title</p>
            <div class="tags">
                <p>tags</p>
            </div>
            <p>description</p>
            <p>course name</p>
            <div class="buttons">buttons</div>
        </div>
    </div>

    <h2>📕Mentorship & Project-based Internship</h2>

    <div class="pbi-section">

    </div>
</template>
<script>
import { Divider } from '#components';
// import axios from "axios";
import CourseProject from '@/data/CourseProject.json';
import PBIProject from '@/data/PBIProject.json';

export default {
  data() {
    return {
      data: CourseProject, PBIProject
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

.porto-section {

}

</style>