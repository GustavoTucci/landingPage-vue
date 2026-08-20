<template>
  <section class="blog-section">
    <div class="blog-container">
      <h2 class="blog-title">Conteúdo para projetar melhor</h2>
      <div class="title-accent"></div>
      
      <div class="blog-grid">
        <article class="blog-post" v-for="post in posts" :key="post.id">
          <div class="post-image">
            <img :src="post.image" :alt="post.title">
          </div>
          <div class="post-content">
            <div class="post-meta">
              <span class="post-category">{{ post.category }}</span>
              <span class="post-date">{{ post.date }}</span>
            </div>
            <h3 class="post-title">{{ post.title }}</h3>
            <p class="post-excerpt">{{ post.excerpt }}</p>
            <a href="#" class="post-link">Ler mais</a>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>

<script>
import './Blog.css'
import img1 from '@/assets/img-1.jpg'
import img2 from '@/assets/img-2.jpg'
import img3 from '@/assets/img-3.jpg'

export default {
  name: 'BlogSection',
  data() {
    return {
      posts: [
        {
          id: 1,
          title: 'Como a visualização arquitetônica valoriza um projeto',
          excerpt: 'Entenda como enquadramento, luz e narrativa ajudam seu projeto a ser compreendido antes mesmo da obra.',
          image: img1,
          category: 'Tendências',
          date: '15 Mar 2024'
        },
        {
          id: 2,
          title: 'Quando usar imagens, animação ou tour virtual',
          excerpt: 'Veja qual formato visual faz mais sentido para apresentar ambientes, vender unidades ou conquistar aprovação.',
          image: img2,
          category: 'Tecnologia',
          date: '12 Mar 2024'
        },
        {
          id: 3,
          title: 'Materiais e luz: o detalhe que muda tudo',
          excerpt: 'Boas escolhas de iluminação e acabamento dão profundidade à imagem e revelam a intenção do projeto.',
          image: img3,
          category: 'Sustentabilidade',
          date: '10 Mar 2024'
        }
      ]
    }
  }
}
</script> 