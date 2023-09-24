<template>
  <div id="about">
    <div class="about-container">
      <div class="about-me">
        <h2>About Me</h2>
        <p>
          Hello! I'm a passionate web developer specializing in both front-end and back-end
          technologies. With a strong focus on user experience, I strive to create web 
          applications that are both functional and visually appealing. My journey in the 
          tech world began with learning the core web technologies—HTML, CSS, and JavaScript—which
          laid the foundation for diving into modern frameworks and libraries such as Vue.js 
          and React. In addition to coding, I have a keen interest in UI/UX design and always 
          aim for a user-centric approach. 
        </p>
        <p>I'm also comfortable working with back-end technologies 
          like Node.js and various databases, ensuring that the applications I develop are not only
          beautiful but also high-performing and secure. The tech industry is ever-evolving, 
          and I'm always on the lookout for new challenges and opportunities for growth. 
          Whether it's problem-solving or learning new technologies, I'm up for the challenge.
        </p>
      </div>
      <div class="skills">
        <h2 class="center-text" style="text-align: center;">My Skills</h2>
        <div class="grid-header">
          <div class="skill-header">Skill</div>
          <div class="exp-header">Experience</div>
        </div>
        <div class="scrollable-section">
          <div class="grid-row" v-for="skill in skills" :key="skill.name">
            <div class="grid-cell">
              <img :src="skill.logo" :alt="`${skill.name} logo`" width="50" />
              <div class="skill-name">{{ skill.name }}</div>
            </div>
            <div class="grid-cell text-center">
              {{ skill.years }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>






<script>
export default {
  data() {
    return {
      skills: [
        { name: 'HTML', logo: require('@/assets/html.png'), years: 3 },
        { name: 'CSS', logo: require('@/assets/css.png'), years: 5 },
        { name: 'JavaScript', logo: require('@/assets/javascript.png'), years: 2 },
        { name: 'Vue.js', logo: require('@/assets/vue.png'), years: 1 },
        { name: 'SQL', logo: require('@/assets/sql.png'), years: 3 },
        
      ],
    };
  },
};
</script>

<style scoped>
#about {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 70vh;
  padding: 2rem;
}

.about-container {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;  
  flex-wrap: wrap;
  width: 100%;
}

.about-me, .skills {
  width: 45%;
  padding: 1rem;
}

.about-me h2, .skills h2 {
  margin: 0;
  padding: 0;
  text-align: center;
}

.about-me p {
  margin-top: 1rem;
  text-align: justify;
}

.skills {
  border: 2px solid #ddd;
  border-radius: 8px;
}

.grid-header, .grid-row {
  display: grid;
  grid-template-columns: 70% 30%;
}

.grid-cell, .skill-header, .exp-header {
  padding: 8px;
  display: flex;
  align-items: center;
}

.grid-header > div {
  background-color: #8aee8d;
  color: rgb(112, 32, 5);
  padding: 8px;
  text-align: center;
}

.grid-row {
  transition: all 0.3s ease;
}

.grid-row:hover {
  background-color: #8422d5;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  color: #333;
  cursor: pointer;
}

.scrollable-section {
  overflow-y: auto;
  max-height: 190px;
  grid-column: 1 / span 2;
}

.skill-name {
  margin-left: 10px;
  text-align: center;
}

.text-center {
  text-align: center;
}

/* Apply styles for mobile screens */
@media (max-width: 768px) {
  .about-me, .skills {
    width: 100%; 
    padding: 1rem;
    margin-top: 1rem; 
  }
}
</style>





<!-- <p>
          Hello! I'm a passionate web developer specializing in both front-end and back-end
          technologies. With a strong focus on user experience, I strive to create web 
          applications that are both functional and visually appealing. My journey in the 
          tech world began with learning the core web technologies—HTML, CSS, and JavaScript—which
          laid the foundation for diving into modern frameworks and libraries such as Vue.js 
          and React. In addition to coding, I have a keen interest in UI/UX design and always 
          aim for a user-centric approach. 
        </p>
        <p>I'm also comfortable working with back-end technologies 
          like Node.js and various databases, ensuring that the applications I develop are not only
          beautiful but also high-performing and secure. The tech industry is ever-evolving, 
          and I'm always on the lookout for new challenges and opportunities for growth. 
          Whether it's problem-solving or learning new technologies, I'm up for the challenge.
        </p> -->