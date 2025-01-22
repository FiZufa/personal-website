<template>
    <h2>🎓Relavant Undergraduate Coursework Projects</h2>

    <div class="porto-section">
        
      <div v-for="(project, index) in data.CourseProject" :key="index" class="projects">
            <h3 style="color: #e43b63;">{{project.name}}</h3>
            <div class="tags">
              <span v-for="(tag, tagIndex) in project.tags" :key="tagIndex" class="tag">
                {{ tag }}
              </span>
            </div>
            <p>{{ project.description }}</p>
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
        <p style="font-style: italic;">{{ project.course }}</p>
        <p style="font-style: italic;">{{ project.period}}</p>
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

.tag {
  background-color: black;
  opacity: 0.8;
  border-radius: 8px;
  color: #fff;
  font-size: 10px;
  padding: 2px 8px;
  margin: 0 2px;
  
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

.button-link.github {
  background-color: #3AA74E; /* GitHub button color */
}

.button-link.slides {
  background-color: #FF5F5F; /* Slides button color */
}

.button-link.prototype {
  background-color: #CEB150;
}


</style>