<template>
    <div id="projects-page">
      <h1>My Projects</h1>
      <div class="projects-container">
        <div class="project-tiles">
          <div
            v-for="project in projects"
            :key="project.id"
            @click="selectProject(project)"
            :class="{ 'selected': selectedProject === project }"
            class="project-tile"
          >
            <img :src="require(`@/assets/${project.image}`)" :alt="project.name" class="project-image" />
          </div>
        </div>
        <div class="project-details">
          <h2>{{ selectedProject ? selectedProject.name : '' }}</h2>
          <p>{{ selectedProject ? selectedProject.description : '' }}</p>
          <a :href="selectedProject ? selectedProject.link : ''" target="_blank">View Project</a>
        </div>
      </div>
    </div>
  </template>
  
  
  
  
  <script>
  export default {
    data() {
      return {
        projects: [
          {
            id: 1,
            name: 'Prop Hire Website',
            description: 'This website was built for a client who has a small diy wedding prop hire business. The client wanted something simple yet elegant while also capturing the core products in her business.',
            link: '#',
            image: 'project1.jpg'
          },
          {
            id: 2,
            name: 'E-commerce Website',
            description: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus ut dui in urna bibendum rhoncus. Proin id ex sed arcu feugiat tincidunt in at ex. Nullam eget fermentum odio.',
            link: '#',
            image: 'project1.jpg'
            },
            {
            id: 3,
            name: 'Portfolio Website',
            description: 'Sed convallis urna nec felis volutpat, sit amet ullamcorper quam posuere. Integer commodo vel risus vel facilisis. Duis at tellus nec neque venenatis auctor.',
            link: '#',
            image: 'project1.jpg'
            },
            {
            id: 4,
            name: 'Mobile App',
            description: 'Phasellus ac velit in sem sollicitudin viverra. Sed a lacinia odio. Fusce tristique, odio non efficitur bibendum, lectus mi interdum odio, nec fringilla purus urna a sapien.',
            link: '#',
            image: 'project1.jpg'
            },
        ],
        selectedProject: null,
      };
    },
    methods: {
      selectProject(project) {
        this.selectedProject = project;
      },
    },
    created() {
      // Select the first project by default
      this.selectedProject = this.projects[0];
    },
  };
  </script>
  
<style scoped>
#projects-page {
  padding: 4rem;
  text-align: center;
}

.projects-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: flex-start;
}

.project-tiles {
  flex: 1;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-evenly;
  align-content: flex-start;
}


.project-tile {
  border: 1px solid #ccc;
  width: 40%; 
  margin-bottom: 1rem;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.project-image {
  width: 100%; 
  height: auto;
  display: block;
  max-height: 200px; 
}

.project-tile:hover {
  background-color: #f5f5f5;
}

.selected {
  border: 2px solid #007bff; 
}


.project-details {
  flex: 1;
  padding: 1rem;
  text-align: left;
}

h1 {
  margin-bottom: 2rem;
}
</style>