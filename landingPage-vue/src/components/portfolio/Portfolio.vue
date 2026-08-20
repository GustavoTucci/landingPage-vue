<template>
  <section id="portfolio" class="portfolio-section">
    <div class="portfolio-container">
      <div class="portfolio-header">
        <span class="portfolio-eyebrow">Nosso trabalho</span>
        <h2 class="section-title">Projetos que ganham vida</h2>
        <p class="portfolio-subtitle">
          Explore uma seleção de projetos em que estratégia, arquitetura e imagem se encontram.
        </p>
      </div>

      <div class="portfolio-filters" role="group" aria-label="Filtrar projetos por categoria">
        <button
          v-for="filter in filters"
          :key="filter.value"
          type="button"
          class="filter-button"
          :class="{ active: activeFilter === filter.value }"
          :aria-pressed="activeFilter === filter.value"
          @click="activeFilter = filter.value"
        >
          {{ filter.label }}
        </button>
      </div>

      <div v-if="filteredProjects.length" class="portfolio-grid">
        <article v-for="project in filteredProjects" :key="project.id" class="project-card">
          <div class="project-image-wrapper">
            <img :src="project.image" :alt="`Imagem do projeto ${project.title}`" class="project-image">
            <span class="project-category">{{ project.categoryLabel }}</span>
          </div>
          <div class="project-content">
            <div>
              <p class="project-type">{{ project.type }}</p>
              <h3>{{ project.title }}</h3>
            </div>
            <span class="project-arrow" aria-hidden="true">↗</span>
          </div>
        </article>
      </div>

      <p v-else class="portfolio-empty">Nenhum projeto encontrado nesta categoria.</p>
    </div>
  </section>
</template>

<script>
import './Portfolio.css'
import img1 from '@/assets/img-1.jpg'
import img2 from '@/assets/img-2.jpg'
import img3 from '@/assets/img-3.jpg'
import backgroundSala from '@/assets/background-sala.jpg'

export default {
  name: 'PortfolioSection',
  data() {
    return {
      activeFilter: 'todos',
      filters: [
        { value: 'todos', label: 'Todos' },
        { value: 'residencial', label: 'Residencial' },
        { value: 'comercial', label: 'Comercial' },
        { value: 'interiores', label: 'Interiores' },
        { value: 'animacao', label: 'Animação' }
      ],
      projects: [
        {
          id: 1,
          title: 'Casa Horizonte',
          type: 'Visualização arquitetônica',
          category: 'residencial',
          categoryLabel: 'Residencial',
          image: img1
        },
        {
          id: 2,
          title: 'Pavilhão Centro',
          type: 'Perspectiva externa',
          category: 'comercial',
          categoryLabel: 'Comercial',
          image: img2
        },
        {
          id: 3,
          title: 'Apartamento Linha',
          type: 'Renderização de interiores',
          category: 'interiores',
          categoryLabel: 'Interiores',
          image: img3
        },
        {
          id: 4,
          title: 'Villa 360',
          type: 'Experiência imersiva',
          category: 'animacao',
          categoryLabel: 'Animação',
          image: backgroundSala
        }
      ]
    }
  },
  computed: {
    filteredProjects() {
      if (this.activeFilter === 'todos') {
        return this.projects
      }

      return this.projects.filter(project => project.category === this.activeFilter)
    }
  }
}
</script>
