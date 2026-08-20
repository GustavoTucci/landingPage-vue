<template>
  <section class="testimonials">
    <div class="testimonials-container">
      <div class="testimonials-header">
        <h2 class="section-title">Projetos vistos por quem confia</h2>
      </div>

      <div class="testimonials-slider" ref="slider">
        <div class="testimonials-track" :style="trackStyle">
          <div v-for="testimonial in testimonials" 
               :key="testimonial.id" 
               class="testimonial-card">
            <div class="testimonial-content">
              <div class="quote-icon">❝</div>
              <p class="testimonial-text">{{ testimonial.text }}</p>
              <div class="testimonial-author">
                <img :src="testimonial.image" :alt="testimonial.name" class="author-image">
                <div class="author-info">
                  <h4>{{ testimonial.name }}</h4>
                  <span>{{ testimonial.role }}, {{ testimonial.company }}</span>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="slider-controls">
        <button class="control-btn prev" @click="prevSlide" :disabled="currentSlide === 0">
          <span>←</span>
        </button>
        <div class="slider-dots">
          <button v-for="(_, index) in testimonials" 
                  :key="index"
                  class="dot"
                  :class="{ active: currentSlide === index }"
                  @click="goToSlide(index)">
          </button>
        </div>
        <button class="control-btn next" @click="nextSlide" 
                :disabled="currentSlide === testimonials.length - 1">
          <span>→</span>
        </button>
      </div>
    </div>
  </section>
</template>

<script>
import './Testimonials.css'
import perfilJoao from '@/assets/perfil-joao.jpg'
import perfilMaria from '@/assets/perfil-maria.jpg'
import perfilPedro from '@/assets/perfil-pedro.jpg'

export default {
  name: 'TestimonialsSection',
  data() {
    return {
      currentSlide: 0,
      testimonials: [
        {
          id: 1,
          text: 'A equipe entendeu a essência do projeto e entregou imagens que facilitaram nossa apresentação ao cliente. O resultado foi preciso e elegante.',
          name: 'João Silva',
          role: 'CEO',
          company: 'TechCorp',
          image: perfilJoao
        },
        {
          id: 2,
          text: 'O processo foi claro do início ao fim. Recebemos um material consistente, com excelente atenção aos detalhes e dentro do prazo combinado.',
          name: 'Maria Santos',
          role: 'Diretora de Marketing',
          company: 'Inovativa',
          image: perfilMaria
        },
        {
          id: 3,
          text: 'A ARCHVIZ transformou nossa visão em uma experiência visual envolvente. As imagens ajudaram o projeto a ser compreendido e lembrado.',
          name: 'Pedro Costa',
          role: 'Arquiteto Chefe',
          company: 'DesignPro',
          image: perfilPedro
        }
      ]
    }
  },
  computed: {
    trackStyle() {
      return {
        transform: `translateX(-${this.currentSlide * 100}%)`
      }
    }
  },
  methods: {
    nextSlide() {
      if (this.currentSlide < this.testimonials.length - 1) {
        this.currentSlide++
      }
    },
    prevSlide() {
      if (this.currentSlide > 0) {
        this.currentSlide--
      }
    },
    goToSlide(index) {
      this.currentSlide = index
    }
  }
}
</script> 