<template>
<div id="contact" class="contact-container">
  <div class="left-col">
    
  </div>
  <div class="right-col">
    
    <h1>Me contacter</h1>
    
    <form id="contact-form" method="post">
      <label for="name">Nom complet</label>
  <input type="text" id="name" name="name" placeholder="Votre nom" required>
      <label for="email">Adresse E-mail</label>
  <input type="email" id="email" name="email" placeholder="Votre adresse e-mail" required>
      <label for="message">Message</label>
  <textarea rows="6" placeholder="Votre Message" id="message" name="message" required></textarea>
      <!--<a href="javascript:void(0)">--><button type="submit" id="submit" name="submit">Envoyer</button><!--</a>-->
  
</form>
<div id="error"></div>
<div id="success-msg"></div>
  </div>
</div>

</template>

<script>
  export default {
    name: 'ContactMe',
  }
  </script>
  
  <!-- Add "scoped" attribute to limit CSS to this component only -->
  <style lang="scss">
      @import "../../public/assets/css/const.scss";
  
      :root {
  --primary-color: #010712;
  --secondary-color: #818386;
  --bg-color: #FCFDFD;
  --button-color: #3B3636;
  --h1-color: #3F444C;
}

[data-theme="dark"] {
  --primary-color: #FCFDFD;
  --secondary-color: #818386;
  --bg-color: #010712;
  --button-color: #818386;
  --h1-color: #FCFDFD;
}

* {
  box-sizing: border-box;
  transition: all 0.3s ease-in-out;
}

.contact-container {
  display: flex;
  width: 100vw;
  height: 100vh;
  background: var(--bg-color);
}

.left-col {
  width: 45vw;
  height: 100%;
  rotate: -90deg;
  background-image: url("../../public/assets/images/contact.jpg");
  background-size: cover;
  background-repeat: no-repeat;
}

.logo {
  width: 10rem;
  padding: 1.5rem;
}

.right-col {
  background: var(--bg-color);
  width: 45vw;
  height: 100%;
  padding: 8rem 2.5rem;
  padding-left: 10rem;
}

h1, label, button, .description {
  font-weight: 400;
  letter-spacing: 0.1rem;
}

h1 {
  color:var(--h1-color);
  text-transform: uppercase;
  font-size: 2.5rem;
  letter-spacing: 0.5rem;
  font-weight: 300;
}

p {
  color: var(--secondary-color);
  font-size: 0.9rem;
  letter-spacing: 0.01rem;
  width: 40vw;
  margin: 0.25rem 0;
}

label, .description {
  color: var(--secondary-color);
  text-transform: uppercase;
  font-size: 0.625rem;
}

form {
  width: 31.25rem;
  position: relative;
  margin-top: 2rem;
  padding: 1rem 0;
}

input, textarea, label {
  width: 40vw;
  display: block;
}

p, placeholder, input, textarea {
  font-family: 'Helvetica Neue', sans-serif;
}

input::placeholder, textarea::placeholder {
  color: var(--primary-color);
}

input, textarea {
  color: var(--primary-color);
  font-weight: 500;
  background: var(--bg-color);
  border: none;
  border-bottom: 1px solid var(--secondary-color);
  padding: 0.5rem 0;
  margin-bottom: 1rem;
  outline: none;
}

textarea {
  resize: none;
}

button {
  text-transform: uppercase;
  font-weight: 300;
  background: var(--button-color);
  color: var(--bg-color);
  width: 10rem;
  height: 2.25rem;
  border: none;
  border-radius: 2px;
  outline: none;
  cursor: pointer;
}

input:hover, textarea:hover, button:hover {
  opacity: 0.5;
}

button:active {
  opacity: 0.8;
}

/* Toggle Switch */

.theme-switch-wrapper {
  display: flex;
  align-items: center;
  text-align: center;
  width: 160px;
  position: absolute;
  top: 0.5rem;
  right: 0;
}

.description {
    margin-left: 1.25rem;
  }

.theme-switch {
  display: inline-block;
  height: 34px;
  position: relative;
  width: 60px;
}

.theme-switch input {
  display:none;
}

.slider {
  background-color: #ccc;
  bottom: 0;
  cursor: pointer;
  left: 0;
  position: absolute;
  right: 0;
  top: 0;
  transition: .4s;
}

.slider:before {
  background-color: #fff;
  bottom: 0.25rem;
  content: "";
  width: 26px;
  height: 26px;
  left: 0.25rem;
  position: absolute;
  transition: .4s;
}

input:checked + .slider {
  background-color: var(--button-color);
}

input:checked + .slider:before {
  transform: translateX(26px);
}

.slider.round {
  border-radius: 34px;
}

.slider.round:before {
  border-radius: 50%;
}

#error, #success-msg {
  width: 40vw;
  margin: 0.125rem 0;
  font-size: 0.75rem;
  text-transform: uppercase;
  font-family: 'Jost';
  color: var(--secondary-color);
  }

  #success-msg {
  transition-delay: 3s;
  }

  </style>