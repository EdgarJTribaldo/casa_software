<script>
    import { fade } from 'svelte/transition';
  </script>
  
  <section class="hero" transition:fade>
    <div class="hero-content">
      <h1>Los negocios digitales funcionan</h1>
      <p>Navega en la digitalizacion encuentra oportunidades y evita a los piratas en tu barco</p>
      <div class="cta-buttons">
        <button class="primary">Consulta Gratis</button>
        <button class="secondary">Ver Proyectos</button>
      </div>
    </div>
    <div>
        
    </div>
  </section>
  
  <style>
    .hero {
      min-height: 90vh;
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 2rem 5%;
      background: linear-gradient(135deg, rgba(26, 26, 46, 0.9) 0%, #16213ee6), 
      url('../assets/img/digitaliza_tu_negocio.jpg') center/cover no-repeat;      
      color: white;
    }
    
    .hero-content {
      max-width: 600px;
    }
    
    h1 {
      font-size: 4.2rem;
      font-weight: 800;
      margin-bottom: 1.5rem;
      line-height: 1;
      background: linear-gradient(45deg, #4CAF50, #2196F3);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }
    
    p {
      font-size: 1.8rem;
      margin-bottom: 2rem;
      color: #e0e0e0;
    }
    
    .cta-buttons {
      display: flex;
      gap: 1rem;
    }
    
    button {
      padding: 1rem 2rem;
      border-radius: 8px;
      font-weight: 600;
      font-size: 1.1rem;
      cursor: pointer;
      transition: transform 0.2s ease;
    }
    
    button:hover {
      transform: translateY(-2px);
    }
    
    .primary {
      background: white;
      border: none;
      color: #16213ee6;
    }
    
    .secondary {
      background: transparent;
      border: 2px solid white;
      color: white;
    }
    
    @keyframes float {
      0% { transform: translateY(0px); }
      50% { transform: translateY(-20px); }
      100% { transform: translateY(0px); }
    }
    
    @media (max-width: 768px) {
      .hero {
        flex-direction: column;
        text-align: center;
        padding: 2rem;
      }
      
      .hero-content {
        margin-bottom: 2rem;
      }
      
      h1 {
        font-size: 2.5rem;
      }
      
      .cta-buttons {
        justify-content: center;
      }
    }
  </style>