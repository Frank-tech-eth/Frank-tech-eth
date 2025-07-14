# 🔵 Crypto Analytics Dashboard - Real-time Cryptocurrency Data

<div align="center">
  <img src="https://img.shields.io/badge/Status-En_Desarrollo-0066cc?style=for-the-badge" alt="Status" />
  <img src="https://img.shields.io/badge/Vue.js-4FC08D?style=for-the-badge&logo=vue.js&logoColor=white" alt="Vue.js" />
  <img src="https://img.shields.io/badge/D3.js-F9A03C?style=for-the-badge&logo=d3.js&logoColor=white" alt="D3.js" />
  <img src="https://img.shields.io/badge/CoinGecko_API-8DC647?style=for-the-badge&logo=coingecko&logoColor=white" alt="CoinGecko API" />
</div>

## 📋 Descripción

Dashboard completo de analytics para criptomonedas que proporciona datos en tiempo real sobre precios, volúmenes, market cap, y tendencias del mercado crypto. Incluye gráficos interactivos, alertas de precio, y análisis técnico.

## ✨ Características

### 📊 Visualización de Datos
- 📈 Gráficos interactivos en tiempo real
- 🎯 KPIs personalizables
- 📱 Diseño responsive para todos los dispositivos
- 🌙 Modo oscuro/claro
- 🔄 Actualizaciones automáticas cada 30 segundos

### 📈 Métricas y Analytics
- 💰 Ventas y ingresos en tiempo real
- 👥 Análisis de usuarios y comportamiento
- 📊 Performance de productos/servicios
- 🌍 Análisis geográfico de datos
- ⏱️ Tendencias temporales

### 🔧 Funcionalidades Avanzadas
- 🔔 Alertas y notificaciones personalizables
- 📧 Reportes automáticos por email
- 🔐 Sistema de roles y permisos
- 📱 App móvil complementaria
- 🔗 Integración con múltiples APIs

## 🛠️ Tecnologías Utilizadas

### Frontend
- **Vue.js 3** - Framework progresivo de JavaScript
- **Composition API** - API de composición de Vue 3
- **Vue Router** - Enrutador oficial de Vue
- **Pinia** - Store de estado para Vue
- **D3.js** - Librería para visualización de datos
- **Chart.js** - Gráficos adicionales
- **Tailwind CSS** - Framework CSS utility-first

### Backend
- **Node.js** - Runtime de JavaScript
- **Express.js** - Framework web minimalista
- **Socket.io** - Comunicación en tiempo real
- **MongoDB** - Base de datos NoSQL
- **Redis** - Cache y sesiones
- **JWT** - Autenticación con tokens

### DevOps
- **Docker** - Contenedores
- **Nginx** - Servidor web y proxy reverso
- **PM2** - Process manager para Node.js
- **Jenkins** - CI/CD pipeline

## 🚀 Instalación

```bash
# Clonar el repositorio
git clone https://github.com/tu-usuario/proyecto-azul.git
cd proyecto-azul

# Instalar dependencias del frontend
cd frontend
npm install

# Instalar dependencias del backend
cd ../backend
npm install

# Configurar variables de entorno
cp .env.example .env
# Editar .env con tus credenciales

# Ejecutar en desarrollo
npm run dev
```

## 📊 Estructura del Proyecto

```
proyecto-azul/
├── frontend/                 # Aplicación Vue.js
│   ├── src/
│   │   ├── components/       # Componentes reutilizables
│   │   │   ├── charts/       # Componentes de gráficos
│   │   │   ├── dashboard/    # Componentes del dashboard
│   │   │   └── ui/           # Componentes de interfaz
│   │   ├── views/            # Páginas de la aplicación
│   │   ├── stores/           # Stores de Pinia
│   │   ├── services/         # Servicios y APIs
│   │   ├── utils/            # Utilidades
│   │   └── assets/           # Recursos estáticos
│   ├── public/               # Archivos públicos
│   └── package.json
├── backend/                  # API Node.js
│   ├── src/
│   │   ├── controllers/      # Controladores
│   │   ├── models/           # Modelos de datos
│   │   ├── routes/           # Rutas de la API
│   │   ├── middleware/       # Middlewares
│   │   ├── services/         # Servicios de negocio
│   │   └── utils/            # Utilidades
│   ├── tests/                # Tests
│   └── package.json
├── docker-compose.yml        # Configuración de Docker
└── README.md
```

## 📈 Tipos de Gráficos Disponibles

### 📊 Gráficos de Línea
- Tendencias temporales
- Comparación de métricas
- Predicciones y forecasting

### 🍩 Gráficos de Dona
- Distribución de ventas por categoría
- Análisis de mercado
- Participación de usuarios

### 📊 Gráficos de Barras
- Comparación de productos
- Análisis de regiones
- Performance por período

### 🗺️ Mapas de Calor
- Análisis geográfico
- Densidad de usuarios
- Distribución de ventas

### 📈 Gráficos de Área
- Volumen de datos
- Análisis de crecimiento
- Tendencias acumulativas

## 🔧 Configuración de KPIs

```javascript
// Ejemplo de configuración de KPI
const kpiConfig = {
  id: 'sales_revenue',
  name: 'Ingresos por Ventas',
  type: 'currency',
  target: 1000000,
  current: 850000,
  format: 'USD',
  updateInterval: 30000, // 30 segundos
  alerts: {
    threshold: 0.8, // 80% del objetivo
    email: ['admin@company.com'],
    slack: '#analytics-alerts'
  }
}
```

## 📱 API Endpoints

### Métricas
- `GET /api/metrics` - Obtener todas las métricas
- `GET /api/metrics/:id` - Obtener métrica específica
- `POST /api/metrics` - Crear nueva métrica
- `PUT /api/metrics/:id` - Actualizar métrica

### Dashboard
- `GET /api/dashboard` - Configuración del dashboard
- `POST /api/dashboard/layout` - Guardar layout personalizado
- `GET /api/dashboard/widgets` - Widgets disponibles

### Alertas
- `GET /api/alerts` - Listar alertas
- `POST /api/alerts` - Crear alerta
- `PUT /api/alerts/:id` - Actualizar alerta

### Reportes
- `GET /api/reports` - Listar reportes
- `POST /api/reports/generate` - Generar reporte
- `GET /api/reports/:id/download` - Descargar reporte

## 🔔 Sistema de Alertas

```javascript
// Configuración de alertas
const alertConfig = {
  type: 'threshold', // threshold, trend, anomaly
  metric: 'sales_revenue',
  condition: 'below',
  value: 800000,
  actions: [
    {
      type: 'email',
      recipients: ['manager@company.com'],
      template: 'sales_alert'
    },
    {
      type: 'slack',
      channel: '#sales-alerts',
      message: 'Las ventas han caído por debajo del umbral'
    },
    {
      type: 'webhook',
      url: 'https://api.company.com/notifications',
      method: 'POST'
    }
  ]
}
```

## 📊 Integración con APIs Externas

### Google Analytics
- Métricas de tráfico web
- Comportamiento de usuarios
- Conversiones y objetivos

### Salesforce
- Datos de CRM
- Pipeline de ventas
- Performance de vendedores

### Shopify
- Datos de e-commerce
- Ventas online
- Inventario y productos

### Stripe
- Transacciones de pagos
- Revenue en tiempo real
- Análisis de fraudes

## 🎨 Temas y Personalización

### Tema Claro
```css
:root {
  --primary-color: #0066cc;
  --secondary-color: #4fc08d;
  --background-color: #ffffff;
  --text-color: #2c3e50;
  --border-color: #e2e8f0;
}
```

### Tema Oscuro
```css
:root {
  --primary-color: #0066cc;
  --secondary-color: #4fc08d;
  --background-color: #1a202c;
  --text-color: #f7fafc;
  --border-color: #4a5568;
}
```

## 📸 Capturas de Pantalla

<div align="center">
  <img src="https://via.placeholder.com/800x400/0066cc/ffffff?text=Dashboard+Principal" alt="Dashboard" width="400" />
  <img src="https://via.placeholder.com/800x400/0066cc/ffffff?text=Gráficos+Interactivos" alt="Charts" width="400" />
  <img src="https://via.placeholder.com/800x400/0066cc/ffffff?text=Configuración+de+KPIs" alt="KPIs" width="400" />
  <img src="https://via.placeholder.com/800x400/0066cc/ffffff?text=Sistema+de+Alertas" alt="Alerts" width="400" />
</div>

## 🧪 Testing

```bash
# Tests del frontend
cd frontend
npm run test:unit
npm run test:e2e

# Tests del backend
cd backend
npm test
npm run test:coverage

# Tests de integración
npm run test:integration
```

## 🚀 Despliegue

### Docker
```bash
# Construir y ejecutar con Docker Compose
docker-compose up -d

# Ver logs
docker-compose logs -f
```

### Producción
```bash
# Configurar variables de entorno de producción
export NODE_ENV=production
export MONGODB_URI=mongodb://production-db
export REDIS_URL=redis://production-redis

# Ejecutar con PM2
pm2 start ecosystem.config.js
```

## 📈 Monitoreo y Performance

### Métricas de Performance
- ⏱️ Tiempo de carga de página
- 🔄 Tiempo de respuesta de API
- 💾 Uso de memoria
- 🖥️ CPU usage

### Herramientas de Monitoreo
- **New Relic** - APM y monitoreo
- **Sentry** - Error tracking
- **Grafana** - Visualización de métricas
- **Prometheus** - Métricas del sistema

## 🤝 Contribuir

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

## 👨‍💻 Autor

**Tu Nombre** - [@tu-usuario](https://github.com/tu-usuario)

---

<div align="center">
  <img src="https://img.shields.io/badge/Made%20with%20%E2%9D%A4%EF%B8%8F-Santiago%20de%20Chile-0066cc?style=for-the-badge" alt="Made with love" />
</div> 