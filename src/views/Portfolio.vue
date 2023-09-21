<template>
  <div>
    <div class="portfolio">
      <div class="aboutme">
        <h2>About Me</h2>
        <p>
          Hi, I’m Stephen and currently studying a Bachelor of Information
          Technology.
        </p>
      </div>
      <div class="hobbies">
        <h2>Hobbies</h2>
        <ul class="listHobbies">
          <li>Swimming</li>
          <li>Cooking</li>
          <li>Board Games</li>
        </ul>
      </div>
      <div class="languages">
        <h2>Programming Languages</h2>
        <div>
          <h1>C#, C++, Python</h1>
        </div>
      </div>
      <div class="Koala">
        <img src="public/KoalaThumbsUp.jpg" alt="Koala thumbs up" />
      </div>
    </div>
  </div>
</template>

<script></script>

<style scoped>
.portfolio {
  display: flex;
  flex-wrap: wrap;
  margin: 50px;
}

.aboutme,
.hobbies {
  flex: 1;
  padding: 20px;
  border: 4px solid #333;
  border-radius: 10px;
  margin: 10px;
  text-align: center;
}

.listHobbies {
  list-style-type: none;
}

.languages {
  flex-basis: 100%;
  text-align: center;
  border: 4px solid #333;
  border-radius: 10px;
  padding: 20px;
  margin-top: 30px;
  margin-left: 400px;
  margin-right: 400px;
}


.Koala {
  flex-basis: 100%;
  text-align: center;
  border: none; 
}

h2 {
  font-size: 24px;
  margin-bottom: 10px;
}

ul {
  list-style-type: disc;
  padding-left: 20px;
}

img {
  max-width: 100%;
  height: auto;
}

@media (max-width: 800px) {
  .portfolio {
    flex-direction: column;
    align-items: center;
  }

  .languages {
    margin-left: 20px;
    margin-right: 20px;
  }

}
</style>
