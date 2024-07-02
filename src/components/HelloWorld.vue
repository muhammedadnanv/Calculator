<template>
  <div class="hello">
    <h1>My name is Muhammed Adnan</h1>
    <p>I am a self-learned developer.</p>
    <a href="https://muhammedadnanavv.vercel.app">Visit Now</a>
  </div>
  
  <div id="intro">
    <h3>If you are a self-learner, you can learn and build projects!</h3>
  </div>
  
  <div id="social-media">
    <h3>Follow me on Social Media</h3>
    <div class="social-buttons">
      <button class="social-button"><a href="https://github.com/muhammedadnanv">Github</a></button>
      <button class="social-button"><a href="https://www.facebook.com/profile.php?id=100084139741037">Facebook</a></button>
      <button class="social-button"><a href="https://www.linkedin.com/in/muhammedadnanvv/">LinkedIn</a></button>
    </div>
  </div>
  
  <div id="contact">
    <h1>Contact me</h1>
    <div class="contact-form">
      <form action="https://formbold.com/s/9XqPy" method="post">
        <label for="name">Enter Name</label><br>
        <input type="text" id="name" name="name"><br>
        
        <label for="email">Enter Email</label><br>
        <input type="email" id="email" name="email"><br><br>
        
        <input type="submit" value="Submit">
      </form>
    </div>
  </div>
</template>

<script>
export default {
  name: 'app',
  data() {
    return {
      // Your data properties if any
    };
  }
};
</script>

<style scoped>
/* Scoped styles for this component only */

.hello {
  text-align: center;
  margin-bottom: 20px;
}

.intro {
  text-align: center;
  margin-bottom: 40px;
}

#social-media {
  text-align: center;
  margin-bottom: 40px;
}

.social-buttons {
  margin-top: 20px;
}

.social-button {
  background-color: black;
  color: gold; /* Adjusted to golden color */
  border: none;
  padding: 10px 20px;
  margin-right: 10px;
  cursor: pointer;
}

.contact-form {
  background-color: gold; /* Adjusted to golden color */
  color: black;
  padding: 20px;
  margin-top: 20px;
}

.contact-form label {
  margin-bottom: 10px;
}

.contact-form input[type="text"],
.contact-form input[type="email"] {
  width: 100%;
  padding: 10px;
  margin-bottom: 10px;
  border: 1px solid black; /* Added border for input fields */
}

.contact-form input[type="submit"] {
  background-color: black;
  color: gold; /* Adjusted to golden color */
  border: none;
  padding: 10px 20px;
  cursor: pointer;
}
</style>
