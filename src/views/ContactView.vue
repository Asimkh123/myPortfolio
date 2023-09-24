<template>
    <div id="contact">
      <h1>Contact Me</h1>
      <form @submit.prevent="sendMessage">
        <div class="form-group">
          <label for="name">Name</label>
          <input type="text" id="name" v-model="name" required />
        </div>
        <div class="form-group">
          <label for="email">Email</label>
          <input type="email" id="email" v-model="email" required />
        </div>
        <div class="form-group">
          <label for="message">Message</label>
          <textarea id="message" v-model="message" required></textarea>
        </div>
        <div class="button-wrapper">
          <button type="submit">Send Message</button>
        </div>
        <div v-if="formSubmitted" class="success-message">
          Your message has been successfully sent!
        </div>
      </form>
      <div class="linkedin-container">
        <img src="@/assets/linkedin.png" alt="LinkedIn Logo" class="linkedin-logo" />
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        name: '',
        email: '',
        message: '',
        formSubmitted: false
      };
    },
    methods: {
      sendMessage() {
        console.log(`Sending message from ${this.name} (${this.email}): ${this.message}`);
        this.formSubmitted = true;
      }
    }
  }
  </script>
  
  <style scoped>
  #contact {
    padding: 4rem;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  
  h1 {
    margin-bottom: 2rem;
    text-align: center;
  }
  
  form {
    width: 100%;
    max-width: 600px;
    padding: 0;
    margin: 0;
  }
  
  .form-group {
    margin-bottom: 2rem;
    position: relative;
  }
  
  label {
    display: block;
    margin-bottom: 0.5rem;
    font-weight: 600;
  }
  
  input,
  textarea {
    width: 100%;
    padding: 1rem;
    border: 1px solid #ccc;
    border-radius: 0.25rem;
    transition: border-color 0.3s ease;
  }
  
  input:focus,
  textarea:focus {
    border-color: #007bff;
    outline: none;
  }
  
  textarea {
    resize: vertical;
    min-height: 100px;
  }
  
  .button-wrapper {
    display: flex;
    justify-content: flex-end;
    padding: 0;
    margin: 0;
  }
  
  button {
    padding: 1rem 2rem;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 0.25rem;
    cursor: pointer;
    transition: background-color 0.3s ease;
    margin: 0;
  }
  
  button:hover {
    background-color: #0056b3;
  }
  
  button:active {
    background-color: #004085;
  }
  
  .success-message {
    margin-top: 1rem;
    padding: 1rem;
    background-color: #D4EDDA;
    color: #155724;
    border: 1px solid #C3E6CB;
    border-radius: 0.25rem;
    text-align: center;
  }
  
  .linkedin-container {
    margin-top: 2rem;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  
  .linkedin-logo {
    width: 48px;
    height: auto;
  }
  </style>
  