<template>
  <section class="pricing">
    <div class="pricing-container">
      <h2 class="section-title">Soluções para cada etapa</h2>
      <div class="title-accent"></div>
      <p class="pricing-subtitle">Escolha o nível de produção que melhor acompanha o momento do seu projeto.</p>
      
      <div class="pricing-grid">
        <div class="price-card">
          <h3>Básico</h3>
          <div class="price">
            <span class="currency">R$</span>
            <span class="amount">99</span>
            <span class="period">/mês</span>
          </div>
          <ul class="features-list">
            <li>Até 3 imagens renderizadas</li>
            <li>1 rodada de ajustes</li>
            <li>Entrega em alta resolução</li>
          </ul>
          <button class="cta-button">Solicitar proposta</button>
        </div>

        <div class="price-card featured">
          <div class="featured-tag">Mais Popular</div>
          <h3>Profissional</h3>
          <div class="price">
            <span class="currency">R$</span>
            <span class="amount">199</span>
            <span class="period">/mês</span>
          </div>
          <ul class="features-list">
            <li>Até 8 imagens renderizadas</li>
            <li>2 rodadas de ajustes</li>
            <li>Direção de luz e materiais</li>
            <li>Imagens para apresentação e divulgação</li>
            <li>Acompanhamento prioritário</li>
          </ul>
          <button class="cta-button featured">Solicitar proposta</button>
        </div>

        <div class="price-card">
          <h3>Enterprise</h3>
          <div class="price">
            <span class="currency">R$</span>
            <span class="amount">299</span>
            <span class="period">/mês</span>
          </div>
          <ul class="features-list">
            <li>Imagens, animações e tour virtual</li>
            <li>Direção visual completa do projeto</li>
            <li>Rodadas de ajustes personalizadas</li>
            <li>Atendimento dedicado</li>
            <li>Arquivos preparados para diferentes mídias</li>
            <li>Planejamento de produção sob medida</li>
          </ul>
          <button class="cta-button">Falar com a equipe</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import './Pricing.css'

export default {
  name: 'PricingSection'
}
</script> 