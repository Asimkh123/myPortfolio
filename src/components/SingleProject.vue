<template>
    <div class="single-project">
      <img :src="require('@/assets/project1.jpg')" alt="Project 1" class="project-image" />
      <h2>{{ project.name }}</h2>
      <p>{{ project.description }}</p>
      <a :href="project.link" target="_blank">View Project</a>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      project: Object
    }
  };
  </script>
  
  <style scoped>
  .single-project {
    border: 1px solid #ccc;
    padding: 1rem;
    margin: 1rem;
    text-align: center;
  }
  
  .project-image {
    width: 100%;
    height: auto;
    margin-bottom: 1rem;
  }
  </style>
  