<script setup>
import { ref, computed } from 'vue'
import participantsData from '../static/participants.json'

const selectedIndustry = ref('All')

const participants = ref(participantsData)

const filteredParticipants = computed(() => {
  return participants.value.filter(p => {
    return selectedIndustry.value === 'All' || p.industry === selectedIndustry.value
  })
})
</script>

<template>
    <div class="py-5 text-light min-vh-100" style="background-color: transparent;">
        <div class="container py-4">
            <!-- Hero & Header Section -->
            <section class="mb-5 text-center">
                <div class="d-flex flex-column gap-2 mb-4">
                    <h1 class="display-6 fw-bold text-white tracking-tight">TechBlazers Directory</h1>
                    <p class="text-white-50 lead fs-6 mx-auto" style="max-width: 500px;">Meet the innovative minds and tech pioneers driving our program forward.</p>
                </div>

                <!-- Simple Filter Tabs (Pill Buttons) -->
                <div class="d-flex justify-content-center gap-2 mb-4">
                    <button 
                        @click="selectedIndustry = 'All'" 
                        class="btn rounded-pill px-4 py-2 small fw-semibold transition-all shadow-none" 
                        :class="selectedIndustry === 'All' ? 'btn-primary bg-primary border-primary' : 'btn-outline-light text-white-50 border-white-opacity-10'"
                    >
                        All
                    </button>
                    <button 
                        @click="selectedIndustry = 'IT'" 
                        class="btn rounded-pill px-4 py-2 small fw-semibold transition-all shadow-none" 
                        :class="selectedIndustry === 'IT' ? 'btn-primary bg-primary border-primary' : 'btn-outline-light text-white-50 border-white-opacity-10'"
                    >
                        IT
                    </button>
                    <button 
                        @click="selectedIndustry = 'Embedded'" 
                        class="btn rounded-pill px-4 py-2 small fw-semibold transition-all shadow-none" 
                        :class="selectedIndustry === 'Embedded' ? 'btn-primary bg-primary border-primary' : 'btn-outline-light text-white-50 border-white-opacity-10'"
                    >
                        Embedded
                    </button>
                </div>
            </section>

            <!-- Minimalist Team Grid -->
            <div class="row row-cols-1 row-cols-md-2 row-cols-lg-3 g-4 mb-4">
                <div v-for="(p, index) in filteredParticipants" :key="index" class="col">
                    <div class="card h-100 border border-white border-opacity-10 rounded-4 p-4 text-center hover-profile-card transition-all" style="background-color: rgba(255, 255, 255, 0.03) !important;">
                        <!-- Profile Avatar -->
                        <div class="position-relative mx-auto mb-3" style="width: 80px; height: 80px;">
                            <img class="img-fluid rounded-circle object-fit-cover border border-white border-opacity-10 w-100 h-100" :src="p.avatar" :alt="p.name"/>
                        </div>
                        
                        <!-- Name & Category -->
                        <h2 class="h5 fw-bold text-white mb-1">{{ p.name }}</h2>
                        <span class="text-uppercase tracking-wider small fw-semibold mb-3 d-block" :class="p.industry === 'IT' ? 'text-cyan' : 'text-gold'" style="font-size: 0.75rem;">
                            {{ p.industry }}
                        </span>
                        
                        <!-- Description -->
                        <p class="text-white-50 small mb-4 px-1" style="line-height: 1.6; font-size: 0.9rem;">
                            {{ p.description }}
                        </p>
                        
                        <!-- Mini Skills List -->
                        <div class="mt-auto pt-3 border-top border-white border-opacity-10">
                            <p class="small text-white-50 opacity-75 mb-0 text-truncate" style="font-size: 0.8rem;">
                                {{ p.skills.join(' · ') }}
                            </p>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Empty State -->
            <div v-if="filteredParticipants.length === 0" class="text-center py-5">
                <p class="text-white-50 fs-5">No participants found matching this category.</p>
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
</style>
