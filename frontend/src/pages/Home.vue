<template>
    <div class="py-5 text-light min-vh-100 d-flex flex-column justify-content-center" style="background-color: transparent;">
        <!-- Hero Section -->
        <section class="text-center py-5 mb-5">
            <div class="container py-4">
                <span class="badge bg-primary px-3 py-2 rounded-pill mb-3 text-uppercase tracking-wider">STMicroelectronics Mentor Program</span>
                <h1 class="display-3 fw-bold text-white mb-4 tracking-tight">
                    Unleashing <span class="brand-gradient">Next-Gen</span> Innovation
                </h1>
                <p class="text-white-50 lead fs-5 mx-auto mb-5" style="max-width: 680px; line-height: 1.7;">
                    TechBlazers is an advanced technical initiative fostering creativity and engineering excellence among young engineers through hands-on industrial projects and real-world microelectronics applications.
                </p>
                <div class="d-flex justify-content-center gap-3 flex-wrap">
                    <RouterLink to="/people" class="btn btn-primary px-4 py-3 rounded-pill fw-semibold shadow-none border-0" style="background-color: #4da3ff;">
                        Meet the Pioneers
                    </RouterLink>
                    <RouterLink to="/projects" class="btn btn-outline-light px-4 py-3 rounded-pill fw-semibold shadow-none border-white-opacity-15">
                        Explore Projects
                    </RouterLink>
                </div>
            </div>
        </section>

        <!-- Features Showcase Section -->
        <section class="py-5 border-top border-white border-opacity-10 bg-black bg-opacity-10">
            <div class="container">
                <div class="row g-4 text-center justify-content-center">
                    <!-- Feature 1 -->
                    <div class="col-md-4">
                        <div class="card h-100 border border-white border-opacity-10 rounded-4 p-4 hover-card transition-all" style="background-color: rgba(255, 255, 255, 0.03) !important;">
                            <div class="feature-icon-wrapper mb-3 mx-auto text-primary d-flex align-items-center justify-content-center rounded-circle" style="width: 56px; height: 56px; background-color: rgba(77, 163, 255, 0.1);">
                                <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" fill="#4da3ff" class="bi bi-cpu" viewBox="0 0 16 16">
                                    <path d="M5 0a.5.5 0 0 1 .5.5V2h1V.5a.5.5 0 0 1 1 0V2h1V.5a.5.5 0 0 1 1 0V2h1V.5a.5.5 0 0 1 1 0V2A2.5 2.5 0 0 1 14 4.5h1.5a.5.5 0 0 1 0 1H14v1h1.5a.5.5 0 0 1 0 1H14v1h1.5a.5.5 0 0 1 0 1H14v1h1.5a.5.5 0 0 1 0 1H14a2.5 2.5 0 0 1-2.5 2.5v1.5a.5.5 0 0 1-1 0V14h-1v1.5a.5.5 0 0 1-1 0V14h-1v1.5a.5.5 0 0 1-1 0V14h-1v1.5a.5.5 0 0 1-1 0V14A2.5 2.5 0 0 1 2 11.5H.5a.5.5 0 0 1 0-1H2v-1H.5a.5.5 0 0 1 0-1H2v-1H.5a.5.5 0 0 1 0-1H2v-1H.5a.5.5 0 0 1 0-1H2A2.5 2.5 0 0 1 4.5 2V.5A.5.5 0 0 1 5 0m-.5 3A1.5 1.5 0 0 0 3 4.5v7A1.5 1.5 0 0 0 4.5 13h7a1.5 1.5 0 0 0 1.5-1.5v-7A1.5 1.5 0 0 0 11.5 3z"/>
                                    <path d="M5 5a1 1 0 0 1 1-1h4a1 1 0 0 1 1 1v4a1 1 0 0 1-1 1H6a1 1 0 0 1-1-1zm1 0v4h4V5z"/>
                                </svg>
                            </div>
                            <h3 class="h5 fw-bold text-white mb-2">Embedded Systems</h3>
                            <p class="text-white-50 small mb-0">
                                Low-power firmware development, STM32 real-time operating systems (RTOS), Edge AI, and smart hardware designs.
                            </p>
                        </div>
                    </div>
                    
                    <!-- Feature 2 -->
                    <div class="col-md-4">
                        <div class="card h-100 border border-white border-opacity-10 rounded-4 p-4 hover-card transition-all" style="background-color: rgba(255, 255, 255, 0.03) !important;">
                            <div class="feature-icon-wrapper mb-3 mx-auto text-primary d-flex align-items-center justify-content-center rounded-circle" style="width: 56px; height: 56px; background-color: rgba(77, 163, 255, 0.1);">
                                <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" fill="#4da3ff" class="bi bi-cloud-arrow-up" viewBox="0 0 16 16">
                                    <path fill-rule="evenodd" d="M7.646 5.146a.5.5 0 0 1 .708 0l2 2a.5.5 0 0 1-.708.708L8.5 6.707V10.5a.5.5 0 0 1-1 0V6.707L6.354 7.854a.5.5 0 1 1-.708-.708z"/>
                                    <path d="M4.406 3.342A5.53 5.53 0 0 1 8 2c2.69 0 4.923 2 5.166 4.579C14.758 6.804 16 8.137 16 9.773 16 11.569 14.502 13 12.687 13H3.781C1.708 13 0 11.366 0 9.318c0-1.763 1.266-3.223 2.942-3.593.143-.863.698-1.723 1.464-2.383m.653.757c-.757.653-1.153 1.44-1.153 2.056v.448l-.445.049C2.064 6.805 1 7.952 1 9.318 1 10.785 2.23 12 3.781 12h8.906C13.98 12 15 10.988 15 9.773c0-1.216-1.02-2.228-2.313-2.228h-.5v-.5C12.188 4.825 10.328 3 8 3a4.53 4.53 0 0 0-2.941 1.1"/>
                                </svg>
                            </div>
                            <h3 class="h5 fw-bold text-white mb-2">Cloud &amp; SaaS</h3>
                            <p class="text-white-50 small mb-0">
                                Scalable backends, high-performance distributed microservices, REST APIs, cloud infrastructure, and modern database structures.
                            </p>
                        </div>
                    </div>

                    <!-- Feature 3 -->
                    <div class="col-md-4">
                        <div class="card h-100 border border-white border-opacity-10 rounded-4 p-4 hover-card transition-all" style="background-color: rgba(255, 255, 255, 0.03) !important;">
                            <div class="feature-icon-wrapper mb-3 mx-auto text-primary d-flex align-items-center justify-content-center rounded-circle" style="width: 56px; height: 56px; background-color: rgba(77, 163, 255, 0.1);">
                                <svg xmlns="http://www.w3.org/2000/svg" width="28" height="28" fill="#4da3ff" class="bi bi-shield-check" viewBox="0 0 16 16">
                                    <path d="M5.338 1.59a61 61 0 0 0-2.837.856.48.48 0 0 0-.328.39c-.554 4.157.726 7.19 2.253 9.188a10.7 10.7 0 0 0 2.287 2.233c.346.244.652.244 1.024 0a10.7 10.7 0 0 0 2.287-2.233c1.527-1.997 2.807-5.031 2.253-9.188a.48.48 0 0 0-.328-.39c-.651-.213-1.75-.56-2.837-.855C9.552 1.29 8.931 1.057 8 1.057c-.93 0-1.552.232-2.662.533zM8 .706c.947 0 1.621.246 2.724.549 1.096.3 2.184.643 2.85.86a1.48 1.48 0 0 1 .933 1.236c.658 4.94-.962 8.354-2.67 10.582a11.7 11.7 0 0 1-2.527 2.49c-.533.375-1.15.375-1.683 0a11.7 11.7 0 0 1-2.528-2.49C2.28 11.646.66 8.232 1.319 3.292a1.48 1.48 0 0 1 .933-1.236c.666-.217 1.754-.56 2.85-.86L8 .706z"/>
                                    <path d="M10.854 6.146a.5.5 0 0 0-.708-.708L7.5 8.086 6.354 6.938a.5.5 0 1 0-.708.708l1.5 1.5a.5.5 0 0 0 .708 0z"/>
                                </svg>
                            </div>
                            <h3 class="h5 fw-bold text-white mb-2">Technical Security</h3>
                            <p class="text-white-50 small mb-0">
                                Hardware cryptography, secure boot loader audits, ARM TrustZone partitioning, network penetration testing, and InfoSec auditing.
                            </p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
    </div>
</template>

<style scoped>
.brand-gradient {
    background: linear-gradient(45deg, #4da3ff, #c084fc);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
}
.tracking-wider {
    letter-spacing: 0.1em;
}
.border-white-opacity-15 {
    border-color: rgba(255, 255, 255, 0.15) !important;
}
.hover-card {
    transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1), box-shadow 0.3s cubic-bezier(0.4, 0, 0.2, 1), border-color 0.3s ease;
}
.hover-card:hover {
    transform: translateY(-6px);
    box-shadow: 0 12px 24px rgba(0, 0, 0, 0.3) !important;
    border-color: rgba(255, 255, 255, 0.15) !important;
}
.btn-outline-light:hover {
    background-color: rgba(255, 255, 255, 0.08);
}
</style>