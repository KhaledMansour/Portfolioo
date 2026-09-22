<template>
  <div style="margin-bottom: 80px;">
    <h1>Hello!</h1>

    <div class="paragraph">
      <div>
        I am a Senior Unity Game Developer with 10 years of experience in 3D application development and software architecture. I specialize in applying strict OOP, Design Patterns, and SOLID principles to build highly optimized gameplay systems, rendering pipelines, and scalable User Interfaces. Currently serving as Lead Unity Game Developer at Gimzat Studio, I have led the technical development of hit hybrid-casual titles like Speed Maze and Colors Sorting, achieving over 5M+ downloads while maintaining steady 60fps performance on mid-range devices.
      </div>
    </div>

    <div class="photo">
      <img src="img/profile-pic.jpg" alt="Profile Picture" /> 
    </div>

    <div style="clear:both"></div>

  </div>
</template>

<style scoped>
.paragraph {
  max-width: 700px;
  margin-bottom: 20px;
}

.photo {
  margin-top: 50px;
  text-align: center;
}

.photo img {
  width: 150px;
  height: 150px;
  object-fit: cover;
  object-position: top center;
  border-radius: 50%;
}

@media only screen and (min-width: 620px){
  .paragraph {
    float: left;
  }

  .photo {
    float: left;
    padding: 10px;
    padding-left: 80px;
  }
}

</style>