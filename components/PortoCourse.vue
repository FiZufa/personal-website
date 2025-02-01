<template>
  <div class="line-1"></div>  
  
  <h2>🎓Relevant Undergraduate Coursework Projects</h2>

    <div class="porto-section">
        
      <div v-for="(project, index) in data.CourseProject" :key="index" class="projects">
            <h3 style="color: #e43b63;">{{project.name}}</h3>
            <div class="tags">
              <span v-for="(tag, tagIndex) in project.tags" :key="tagIndex" class="tag">
                {{ tag }}
              </span>
            </div>
            <p>{{ project.description }}</p>
            <p>Skills: 
              <span v-for="(skill, skillIndex) in project.skills" :key="skillIndex" class="skill">
                {{ skill }}
              </span>
            </p>
            <p style="font-style: italic;">{{ project.course }}</p>
            <div class="buttons">
              <a
                v-for="(link, linkName) in project.links"
                :key="linkName"
                :href="link"
                target="_blank"
                :class="['button-link', linkName.toLowerCase()]"
              >   
                {{ linkName }}
              </a>
            </div>
      </div>
    </div>

    <div class="line"></div>

    <h2>📕Mentorship & Project-based Internship</h2>

    <div class="pbi-section">

      <div v-for="(project, index) in data.PBIProject" :key="index" class="pbi-projects">
        <h3 style="color: #e43b63;">{{project.name}}</h3>
        <div class="tags">
          <span v-for="(tag, tagIndex) in project.tags" :key="tagIndex" class="tag">
            {{ tag }}
          </span>
        </div>
        <p>{{ project.description }}</p>
        <p>Skills: 
          <span v-for="(skill, skillIndex) in project.skills" :key="skillIndex" class="skill">
            {{ skill }}
          </span>
        </p>
        <p style="font-style: italic;">{{ project.course }}</p>
        <p>{{ project.period}}</p>
        <div class="buttons">
          <a
            v-for="(link, linkName) in project.links"
            :key="linkName"
            :href="link"
            target="_blank"
            :class="['button-link', linkName.toLowerCase()]"
          >   
            {{ linkName }}
          </a>
        </div>
        
      </div>

    </div>

</template>
<script>
import CourseProject from '@/data/CourseProject.json';
import PBIProject from '@/data/PBIProject.json';
import { Divider } from '#components';
import { Footer } from '#components';

export default {
  data() {
    return {
      data: {
        CourseProject,
        PBIProject,
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

h2 {
  font-weight: normal; /* Makes the text not bold */
}

.porto-section {
  line-height: 1.2;
}

.projects h3, .pbi-projects h3 {
  margin-bottom: 4px;
}

.tags{
  margin-bottom: 2px;
}

.projects p, .pbi-projects p {
  margin: 8px 0;
}

.projects, .pbi-projects {
  margin: 24px 0;
}

.tag {
  background-color: black;
  opacity: 0.8;
  border-radius: 8px;
  color: #fff;
  font-size: 10px;
  padding: 2px 8px;
  margin: -2px 2px;
  
}

.skill {
  background-color: #ccc;
  border-radius: 2px;
  padding: 1px 8px;
  margin: 2px 2px;
  font-size: 12px;
}

.button-link {
  padding: 8px 16px;
  text-decoration: none;
  background-color: #2F86FF;
  border-radius: 4px;
  color: #fff;
  margin: 0 4px;
  display: inline-block;
}

.button-link:hover {
  background-color: #2374e6;
}

.button-link.github {
  background-color: #3AA74E; /* GitHub button color */
}

.button-link.github:hover {
  background-color: #2f9a42;
}

.button-link.slides {
  background-color: #FF5F5F; /* Slides button color */
}

.button-link.slides:hover {
  background-color: #e65050;
}

.button-link.prototype {
  background-color: #CEB150;
}

.button-link.prototype:hover {
  background-color: #bea03f;
}
.line {
  border-top: #ccc solid 1px;
  margin: 48px 0;
}

.line-1 {
  border-top: #ccc solid 1px;
  margin: 32px 0;
}


</style>