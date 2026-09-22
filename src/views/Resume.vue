<template>
  <div>
    <h1>Resume</h1>

    <div class="paragraph">
      I am Khaled Mansour, a Senior Unity Game Developer and Technical Lead with 10 years of experience in full-cycle 3D application development and software architecture.
      <br /><br />
      Throughout my career, I have specialized in applying strict OOP, Design Patterns, and SOLID principles to build highly optimized gameplay systems, rendering pipelines, and scalable User Interfaces. I have successfully led the technical development of hit hybrid-casual titles, achieving over 5M+ downloads while maintaining a steady 60fps performance on mid-range devices.
      <br /><br />
      Whether integrating complex SDKs, programming dynamic auto-solver algorithms, or collaborating with cross-functional design teams, my focus is always on delivering stable, high-performance products within strict release cycles.
      <br /><br />
      I am always eager to tackle complex engineering challenges. If you have an opportunity, feel free to 
      <router-link to="/contact">contact me</router-link>.

      <div style="margin-top:20px; margin-bottom:20px;">
        <a class="download-link" href="d/Khaled_Mansour_CV_.pdf" target="_blank"><i class="fa fa-download fa-lg fa-fw"></i> Download as PDF 🇬🇧</a>
        <div style="clear:both"></div>
      </div>
    </div>
    <div class="photo">
      <img src="img/profile-pic.jpg" alt="Profile Picture" />
    </div>

    <div style="clear:both"></div>

    <div class="full-content">
      <h2>Work experience</h2>

      <h3>Lead Unity Game Developer - Gimzat Studio</h3>
      <h4>2020 - Present</h4>
      <div>Led the technical development of hybrid-casual and puzzle games from initial GDD to global launch. Built core architectures for hit titles like Speed Maze (5M+ downloads) and Colors Sorting (5M+ downloads). Handled performance profiling (Unity Profiler, Xcode Instruments) to hit 60fps via object pooling and draw call batching. Managed native cross-platform builds and complex SDK mediation (Firebase, AppLovin MAX, AdMob, Adjust).</div>
      <div class="tech-stack">C#, Unity URP, iOS/Android SDKs, DOTween.</div>

      <h3>Extended Outsource Partner - Various International Companies</h3>
      <h4>2021 - Present</h4>
      <div>Developed multiple localized multiplayer board and sports games (Bowling Online, Ludo, Domino, Pool & Snooker) for telecom providers. Implemented real-time multiplayer (2-4 players), text chat, and voice chat for global distribution. Developed enterprise VR projects for Johnson & Johnson.</div>
      <div class="tech-stack">Photon Multiplayer, VR (Oculus/Vive), REST APIs.</div>

      <h3>Senior Game Developer - PlaiiMake & Hub43</h3>
      <h4>2019 - 2020</h4>
      <div>Handled mechanics and systems for NEOXPERIENCES' casual games, shipping 4 titles. Concurrently developed space gameplay mechanics, Photon networking, and Node.js backend services at Hub43.</div>
      <div class="tech-stack">C#, Unity, Node.js, MongoDB, Jest.</div>

      <h3>Game Developer - FunRock & Cryptyd</h3>
      <h4>2017 - 2019</h4>
      <div>Enhanced and scaled features for a complex mobile strategy game (Ethad Al Abtal), focusing on client-side optimization. Developed new gameplay systems and Photon multiplayer features for the card game Baloot Quest.</div>
      <div class="tech-stack">C#, Unity, Client-side Optimization.</div>

      <h2>Skills</h2>

      <div class="skill-set">
        <h3>Core Engineering</h3>
        <SkillRate name="C#" :rate="5" />
        <SkillRate name="OOP & SOLID Principles" :rate="5" />
        <SkillRate name="System Architecture" :rate="5" />
        <SkillRate name="3D Optimization" :rate="5" />
        <SkillRate name="Auto-solver Algorithms" :rate="4" />
      </div>

      <div class="skill-set">
        <h3>Engine & Tools</h3>
        <SkillRate name="Unity (URP)" :rate="5" />
        <SkillRate name="Photon Multiplayer" :rate="4" />
        <SkillRate name="Firebase" :rate="4" />
        <SkillRate name="Git & Git LFS" :rate="5" />
        <SkillRate name="Jira" :rate="5" />
        <SkillRate name="Jenkins CI/CD" :rate="4" />
      </div>

      <div class="skill-set">
        <h3>Platforms & Integrations</h3>
        <SkillRate name="Android SDK" :rate="4" />
        <SkillRate name="iOS Publishing (CocoaPods)" :rate="4" />
        <SkillRate name="Ad Mediation (AppLovin, AdMob)" :rate="5" />
        <SkillRate name="VR (Oculus/Vive)" :rate="4" />
      </div>
      <div style="clear:both" />

      <h2>Education</h2>

      <h3>B.Sc. in Computer Science - Suez Canal University</h3>
      <h4>2012 - 2016</h4>
      <div>Graduation Project: 3D Interactive Simulation for E-Learning (Top 5 by TIEC Egypt).</div>

      <h3>Diploma in Game Development - ITI, Giza</h3>
      <h4>2016 - 2017</h4>
      <div>Intensive Game Development Diploma.</div>

      <h2>Languages</h2>

      <h3>Arabic</h3>
      <div>Native</div>

      <h3>English</h3>
      <div>Very Good - professional proficiency for technical documentation and international collaboration.</div>

      <h2>Besides...</h2>
      <div>
        <h3>I 💻 Architecture</h3>
        <div>I am deeply passionate about clean code, scalable systems, and researching new design patterns to solve complex logic puzzles.</div>

        <h3>I 🚀 Performance Optimization</h3>
        <div>I find it genuinely satisfying to dive into the profiler and shave milliseconds off frame times to achieve a flawless 60fps.</div>

        <h3>I 🥽 VR/XR Tech</h3>
        <div>Beyond mobile, I enjoy exploring the boundaries of spatial computing and immersive 3D mechanics.</div>

      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import SkillRate from "@/components/SkillRate.vue";

export default Vue.extend({
  name: "Resume",
  components: {
    SkillRate,
  },
});
</script>

<style scoped>
h2 {
  font-weight: 100;
  font-size: 2em;
  margin: 0px;
  padding: 0px;
  padding-top: 50px;
}
h3 {
  font-weight: 100;
  font-size: 1.6em;
  margin: 0px;
  padding: 0px;
  padding-top: 30px;
}
h4 {
  font-weight: 100;
  font-size: 1.3em;
  margin: 0px;
  padding: 0px;
  padding-top: 15px;
  font-style: italic;
}

.paragraph {
  max-width: 700px;
}

.download-link {
  float:left;
  margin-right: 50px;
}

.full-content div {
  max-width: 800px;
}

.skill-set h3 {
  padding-bottom: 10px;
}

.photo img {
  width: 150px;
  height: 150px;
  object-fit: cover;
  object-position: top center;
  border-radius: 50%;
}

.tech-stack {
  font-style: italic;
}

.photo {
  margin-top: 50px;
  text-align: center;
}

@media only screen and (min-width: 620px){
  .paragraph {
    float: left;
  }

  .photo {
    float: left;
    padding: 30px;
    padding-left: 80px;
  }

  .skill-set {
    float: left;
    padding-right: 60px; 
  }
}
</style>