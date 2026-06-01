<script setup>
import { ref, computed } from 'vue'
import projectsData from '../static/projects.json'

const selectedCategory = ref('All')

const projects = ref(projectsData)

const filteredProjects = computed(() => {
  return projects.value.filter(p => {
    return selectedCategory.value === 'All' || p.category === selectedCategory.value
  })
})
</script>

<template>
    <div class="py-5 text-light min-vh-100" style="background-color: transparent;">
        <div class="container py-4">
            <!-- Hero & Header Section -->
            <section class="mb-5 text-center">
                <div class="d-flex flex-column gap-2 mb-4">
                    <h1 class="display-6 fw-bold text-white tracking-tight">TechBlazers Projects</h1>
                    <p class="text-white-50 lead fs-6 mx-auto" style="max-width: 500px;">Explore the industrial precision systems and digital infrastructures we are building.</p>
                </div>

                <!-- Simple Filter Tabs (Pill Buttons) -->
                <div class="d-flex justify-content-center gap-2 mb-4">
                    <button 
                        @click="selectedCategory = 'All'" 
                        class="btn rounded-pill px-4 py-2 small fw-semibold transition-all shadow-none" 
                        :class="selectedCategory === 'All' ? 'btn-primary bg-primary border-primary' : 'btn-outline-light text-white-50 border-white-opacity-10'"
                    >
                        All
                    </button>
                    <button 
                        @click="selectedCategory = 'IT'" 
                        class="btn rounded-pill px-4 py-2 small fw-semibold transition-all shadow-none" 
                        :class="selectedCategory === 'IT' ? 'btn-primary bg-primary border-primary' : 'btn-outline-light text-white-50 border-white-opacity-10'"
                    >
                        IT
                    </button>
                    <button 
                        @click="selectedCategory = 'Embedded'" 
                        class="btn rounded-pill px-4 py-2 small fw-semibold transition-all shadow-none" 
                        :class="selectedCategory === 'Embedded' ? 'btn-primary bg-primary border-primary' : 'btn-outline-light text-white-50 border-white-opacity-10'"
                    >
                        Embedded
                    </button>
                </div>
            </section>

            <!-- Minimalist Projects Grid -->
            <div class="row row-cols-1 row-cols-md-2 g-4 mb-4">
                <div v-for="(project, index) in filteredProjects" :key="index" class="col">
                    <div class="card h-100 border border-white border-opacity-10 bg-white bg-opacity-5 rounded-4 p-4 hover-profile-card transition-all" style="background-color: rgba(255, 255, 255, 0.03) !important;">
                        <!-- Category Header -->
                        <div class="d-flex justify-content-between align-items-center mb-3">
                            <span class="text-uppercase tracking-wider small fw-semibold" :class="project.category === 'IT' ? 'text-cyan' : 'text-gold'" style="font-size: 0.75rem;">
                                {{ project.category }}
                            </span>
                            <div class="project-dot" :style="project.category === 'IT' ? 'background-color: #4da3ff;' : 'background-color: #ffd200;'"></div>
                        </div>

                        <!-- Title -->
                        <h2 class="h4 fw-bold text-white mb-3">{{ project.title }}</h2>

                        <!-- Description -->
                        <p class="text-white-50 small mb-4 line-height-relaxed" style="line-height: 1.6;">
                            {{ project.description }}
                        </p>

                        <!-- Mini Skills List -->
                        <div class="mt-auto pt-3 border-top border-white border-opacity-10">
                            <p class="small text-white-50 opacity-75 mb-0 text-truncate" style="font-size: 0.8rem;">
                                {{ project.skills.join(' · ') }}
                            </p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Empty State -->
            <div v-if="filteredProjects.length === 0" class="text-center py-5">
                <p class="text-white-50 fs-5">No projects found matching this category.</p>
            </div>
        </div>
    </div>
</template>

<style scoped>
.hover-profile-card {
    transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1), box-shadow 0.3s cubic-bezier(0.4, 0, 0.2, 1), border-color 0.3s ease;
}
.hover-profile-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 25px rgba(0, 0, 0, 0.4) !important;
    border-color: rgba(255, 255, 255, 0.2) !important;
}
.text-cyan {
    color: #4da3ff !important;
}
.text-gold {
    color: #ffd200 !important;
}
.border-white-opacity-10 {
    border-color: rgba(255, 255, 255, 0.1) !important;
}
.btn-outline-light {
    border-color: rgba(255, 255, 255, 0.1);
}
.btn-outline-light:hover {
    background-color: rgba(255, 255, 255, 0.1);
    color: #ffffff !important;
}
.project-dot {
    width: 8px;
    height: 8px;
    border-radius: 50%;
}
</style>