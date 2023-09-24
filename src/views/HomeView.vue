<template>
  <section id="home">
    <div class="container">
      <div class="profile-section">
        <img src="@/assets/profile-pic.jpeg" alt="Profile Pic">
        <h1>Asim Wadood Khan</h1>
        <h2>Software Developer</h2>
        <p>Aspiring Developer and tech enthusiast.</p>
        <button @click="goToProjects">My Projects</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  methods: {
    goToProjects() {
      this.$router.push('/projects');
    }
  }
}
</script>

<style scoped>
  #home {
    padding: 100px 0;
    background-color: #f8f9fa;
    color: #333;
  }

  .profile-section {
    text-align: center;
  }

  .profile-section img {
    max-width: 200px;
    border-radius: 50%;
  }

  h1 {
    font-size: 3em;
  }

  h2 {
    font-size: 2em;
  }

  p {
    font-size: 1.1em;
  }

  button {
    padding: 10px 20px;
    background-color: #007BFF;
    color: #fff;
    border: none;
    border-radius: 5px;
  }
</style>
