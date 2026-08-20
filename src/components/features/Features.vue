<template>
  <section id="servicos" class="features">
    <div class="features-container">
      <h2 class="section-title">Precisão em cada detalhe</h2>
      
      <div class="features-grid">
        <FeatureCard
          v-for="feature in features"
          :key="feature.id"
          :feature="feature"
          class="animate-up"
        />
      </div>
    </div>
  </section>
</template>

<script>
import './Features.css'
import FeatureCard from './FeatureCard.vue'

export default {
  name: 'FeaturesSection',
  components: {
    FeatureCard
  },
  data() {
    return {
      features: [
        {
          id: 1,
          icon: '01',
          title: 'Prazos que respeitam o projeto',
          description: 'Um processo organizado para você apresentar cada etapa com segurança.',
          color: '#C4B19C'
        },
        {
          id: 2,
          icon: '02',
          title: 'Imagens que comunicam',
          description: 'Composição, luz e materiais pensados para valorizar a intenção do projeto.',
          color: '#D4C5B4'
        },
        {
          id: 3,
          icon: '03',
          title: 'Parceria do briefing à entrega',
          description: 'Alinhamento próximo para transformar referências em uma narrativa visual consistente.',
          color: '#E5D5C5'
        }
        // Adicione mais features conforme necessário
      ]
    }
  }
}
</script> 