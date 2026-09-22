<template>
    <div>
      <div class="projects-list">
        <template v-for="project in projects">
          <div
            :key="project.id"
            @click="showDetails(project)"
            class="project-card">
            
            <img :src="project.iconUrl" alt="Game Banner" class="card-banner" />
            
            <div class="card-content">
              <h3 class="card-title">{{ project.name }}</h3>
              <div class="card-icons">
                <i class="fa fa-android fa-lg"></i>
                <i class="fa fa-apple fa-lg"></i>
              </div>
            </div>
          </div>
        </template>
      </div>

      <ProjectDetailsOverlay
        v-on:close="showPopup = false"
        :visible="showPopup"
        :title="popupTitle"
        :htmlContent="popupContent"
        :color="popupColor"
      />
    </div>
</template>

<script lang="ts">
import Vue from "vue";
import ProjectDetailsOverlay from "@/components/ProjectDetailsOverlay.vue";
import ProjectData from "@/data/ProjectData.ts";

export default Vue.extend({
  name: "ProjectsList",
  components: {
    ProjectDetailsOverlay,
  },
  props: {
    projects: Array
  },
  data: function () {
    return {
      showPopup: false,
      popupTitle: "",
      popupColor: "",
      popupContent: ""
    };
  },
  methods: {
    showDetails: function (item: ProjectData) {
      this.popupTitle = item.name;
      this.popupColor = item.accentColor;
      this.popupContent = item.htmlDescription;
      this.showPopup = true;
      window.scrollTo(0,0);
    },
  },
});
</script>

<style scoped>
.projects-list {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(280px, 1fr));
  gap: 25px;
  max-width: 1000px;
  margin: 0 auto;
}

.project-card {
  background-color: #2c2c2c;
  border-radius: 12px;
  overflow: hidden;
  cursor: pointer;
  display: flex;
  flex-direction: column;
  transition: transform 0.3s ease, box-shadow 0.3s ease;
  height: 320px;
  position: relative;
}

.project-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.5);
}

.card-banner {
  width: 100%;
  height: 180px;
  object-fit: contain;
  background-color: #1e1e1e; /* Adds a slightly darker background for letterboxing */
}

.card-content {
  padding: 15px;
  flex: 1;
  display: flex;
  flex-direction: column;
  color: #ffffff;
}

.card-title {
  margin: 0;
  font-size: 1.2rem;
  font-weight: bold;
}

.card-icons {
  position: absolute;
  bottom: 15px;
  left: 15px;
  display: flex;
  gap: 15px;
  color: #aaaaaa;
}
</style>