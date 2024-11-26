<script>
    import { fade } from 'svelte/transition';

    const services = [
        {
            title: "Desarrollo Web",
            description: "Sitios web y aplicaciones personalizadas con las últimas tecnologías para maximizar tu presencia digital.",
            icon: "🌐",
            features: ["Diseño Responsivo", "SEO Optimizado", "Alto Rendimiento"]
        },
        {
            title: "Apps Móviles",
            description: "Aplicaciones nativas y multiplataforma que conectan tu negocio con usuarios en cualquier dispositivo.",
            icon: "📱",
            features: ["iOS y Android", "Experiencia Fluida", "Notificaciones Push"]
        },
        {
            title: "E-Commerce",
            description: "Soluciones completas de comercio electrónico para vender tus productos en línea.",
            icon: "🛍️",
            features: ["Pagos Seguros", "Gestión de Inventario", "Análisis de Ventas"]
        },
        {
            title: "Cloud Services",
            description: "Servicios en la nube escalables y seguros para tu infraestructura digital.",
            icon: "☁️",
            features: ["Alta Disponibilidad", "Backups Automáticos", "Soporte 24/7"]
        }
    ];
</script>

<section class="services" transition:fade>
    <div class="services-header">
        <h2>Nuestros Servicios</h2>
        <p>Soluciones digitales completas para hacer crecer tu negocio</p>
    </div>

    <div class="services-grid">
        {#each services as service}
            <div class="service-card">
                <div class="service-icon">{service.icon}</div>
                <h3>{service.title}</h3>
                <p>{service.description}</p>
                <ul class="features-list">
                    {#each service.features as feature}
                        <li>{feature}</li>
                    {/each}
                </ul>
                <button class="learn-more">Saber más</button>
            </div>
        {/each}
    </div>
</section>

<style>
    .services {
        padding: 5rem 5%;
        background: #f8f9fa;
    }

    .services-header {
        text-align: center;
        margin-bottom: 4rem;
    }

    .services-header h2 {
        font-size: 2.5rem;
        color: #1a1a2e;
        margin-bottom: 1rem;
        background: linear-gradient(45deg, #4CAF50, #2196F3);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
    }

    .services-header p {
        font-size: 1.2rem;
        color: #666;
        max-width: 600px;
        margin: 0 auto;
    }

    .services-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 2rem;
        padding: 1rem;
    }

    .service-card {
        background: white;
        padding: 2rem;
        border-radius: 15px;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        transition: transform 0.3s ease, box-shadow 0.3s ease;
    }

    .service-card:hover {
        transform: translateY(-5px);
        box-shadow: 0 8px 12px rgba(0, 0, 0, 0.15);
    }

    .service-icon {
        font-size: 3rem;
        margin-bottom: 1rem;
    }

    .service-card h3 {
        font-size: 1.5rem;
        color: #1a1a2e;
        margin-bottom: 1rem;
    }

    .service-card p {
        color: #666;
        margin-bottom: 1.5rem;
        line-height: 1.6;
    }

    .features-list {
        list-style: none;
        padding: 0;
        margin-bottom: 1.5rem;
    }

    .features-list li {
        padding: 0.5rem 0;
        color: #4a4a4a;
        display: flex;
        align-items: center;
        gap: 0.5rem;
    }

    .features-list li::before {
        content: "✓";
        color: #4CAF50;
        font-weight: bold;
    }

    .learn-more {
        background: transparent;
        border: 2px solid #4CAF50;
        color: #4CAF50;
        padding: 0.8rem 1.5rem;
        border-radius: 8px;
        font-weight: 600;
        cursor: pointer;
        transition: all 0.3s ease;
    }

    .learn-more:hover {
        background: #4CAF50;
        color: white;
    }

    @media (max-width: 768px) {
        .services {
            padding: 3rem 1rem;
        }

        .services-header h2 {
            font-size: 2rem;
        }

        .services-grid {
            grid-template-columns: 1fr;
        }
    }
</style>
