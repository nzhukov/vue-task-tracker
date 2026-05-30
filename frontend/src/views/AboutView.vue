<template>
    <div class="about-page">
        <!-- Об авторе -->
        <section class="hero">
        <div class="hero-content">
            <h1 class="roboto-condensed-section-title"> Об авторе</h1>
            <p class="hero-subtitle">
            Nikolai Zhukov
            </p>
        </div>
        <p class="error-path">
            Запрошенный путь: <code>{{ currentPath }}</code>
        </p>
        </section>
    </div>
</template>

<script setup>
import { computed } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()

const currentPath = computed(() => route.fullPath)
</script>


<style scoped>
/* Hero */
.roboto-condensed-section-title {
  font-family: "Roboto Condensed", sans-serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-size: 64px;
  font-style: normal;
}


.hero {
  text-align: center;
  padding: 60px 20px;
  background: linear-gradient(135deg, var(--primary-dark) 0%, #4a6fa5 100%);
  border-radius: var(--radius);
  color: white;
  margin-bottom: 40px;
}

.hero-title {
  font-size: 48px;
  margin-bottom: 16px;
}

.hero-subtitle {
  font-size: 20px;
  opacity: 0.9;
  margin-bottom: 32px;
}


</style>
