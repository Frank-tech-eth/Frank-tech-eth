# 🟡 Proyecto Amarillo - App de Delivery de Comida

<div align="center">
  <img src="https://img.shields.io/badge/Status-En_Planificación-ffd700?style=for-the-badge" alt="Status" />
  <img src="https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React Native" />
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase" />
  <img src="https://img.shields.io/badge/Expo-000000?style=for-the-badge&logo=expo&logoColor=white" alt="Expo" />
</div>

## 📋 Descripción

Aplicación móvil completa para delivery de comida que conecta restaurantes con clientes. Incluye funcionalidades de pedidos en tiempo real, seguimiento GPS, pagos integrados y sistema de calificaciones.

## ✨ Características Planificadas

### 👤 Cliente
- 📱 Interfaz intuitiva y fácil de usar
- 🍽️ Catálogo de restaurantes con menús
- 🛒 Carrito de compras con múltiples items
- 📍 Seguimiento en tiempo real del pedido
- 💳 Pagos seguros con múltiples métodos
- ⭐ Sistema de calificaciones y reseñas
- 🔔 Notificaciones push para actualizaciones

### 🏪 Restaurante
- 📊 Dashboard de pedidos en tiempo real
- ⏰ Gestión de horarios y disponibilidad
- 📈 Reportes de ventas y estadísticas
- 🚚 Gestión de repartidores
- 📱 App móvil para restaurantes

### 🚚 Repartidor
- 📍 Navegación GPS integrada
- 📋 Lista de pedidos pendientes
- 💬 Chat con clientes y restaurantes
- 📊 Historial de entregas
- 💰 Sistema de comisiones

## 🛠️ Tecnologías Planificadas

### Frontend Móvil
- **React Native** - Framework para apps móviles
- **Expo** - Plataforma de desarrollo
- **TypeScript** - Tipado estático
- **React Navigation** - Navegación entre pantallas
- **React Native Maps** - Integración de mapas
- **React Native Elements** - Componentes UI

### Backend y Servicios
- **Firebase** - Backend as a Service
  - **Firestore** - Base de datos NoSQL
  - **Authentication** - Autenticación de usuarios
  - **Cloud Functions** - Funciones serverless
  - **Cloud Messaging** - Notificaciones push
  - **Storage** - Almacenamiento de archivos

### APIs Externas
- **Google Maps API** - Mapas y geolocalización
- **Stripe** - Procesamiento de pagos
- **Twilio** - SMS y notificaciones
- **Cloudinary** - Optimización de imágenes

## 📱 Estructura de la App

```
src/
├── components/          # Componentes reutilizables
│   ├── ui/             # Componentes de interfaz
│   ├── forms/          # Formularios
│   └── maps/           # Componentes de mapas
├── screens/            # Pantallas de la app
│   ├── auth/           # Autenticación
│   ├── home/           # Pantalla principal
│   ├── restaurant/     # Detalles de restaurante
│   ├── cart/           # Carrito de compras
│   ├── orders/         # Historial de pedidos
│   └── profile/        # Perfil de usuario
├── navigation/         # Configuración de navegación
├── services/           # Servicios y APIs
├── hooks/              # Custom hooks
├── utils/              # Utilidades y helpers
├── constants/          # Constantes de la app
└── types/              # Tipos TypeScript
```

## 🚀 Plan de Desarrollo

### Fase 1: MVP (Mes 1-2)
- [ ] Configuración del proyecto con Expo
- [ ] Autenticación de usuarios
- [ ] Lista básica de restaurantes
- [ ] Carrito de compras simple
- [ ] Proceso de pedido básico

### Fase 2: Funcionalidades Core (Mes 3-4)
- [ ] Integración con mapas
- [ ] Seguimiento en tiempo real
- [ ] Sistema de pagos
- [ ] Notificaciones push
- [ ] Calificaciones y reseñas

### Fase 3: Optimización (Mes 5-6)
- [ ] Performance y optimización
- [ ] Tests unitarios y de integración
- [ ] App para restaurantes
- [ ] App para repartidores
- [ ] Analytics y métricas

## 📊 Arquitectura de Datos

```javascript
// Estructura de datos en Firestore

// Colección: users
{
  id: "user123",
  name: "Juan Pérez",
  email: "juan@email.com",
  phone: "+56912345678",
  address: {
    street: "Av. Providencia 123",
    city: "Santiago",
    coordinates: { lat: -33.4489, lng: -70.6693 }
  },
  orders: ["order1", "order2"],
  createdAt: timestamp
}

// Colección: restaurants
{
  id: "restaurant456",
  name: "Pizza Express",
  description: "Las mejores pizzas de Santiago",
  cuisine: "Italiana",
  rating: 4.5,
  deliveryTime: "30-45 min",
  minimumOrder: 5000,
  menu: [
    {
      id: "pizza1",
      name: "Pizza Margherita",
      price: 12000,
      description: "Salsa de tomate, mozzarella, albahaca",
      image: "url_to_image"
    }
  ],
  location: {
    address: "Av. Las Condes 789",
    coordinates: { lat: -33.4186, lng: -70.5752 }
  }
}

// Colección: orders
{
  id: "order789",
  userId: "user123",
  restaurantId: "restaurant456",
  items: [
    {
      menuItemId: "pizza1",
      quantity: 2,
      price: 12000
    }
  ],
  total: 24000,
  status: "preparing", // pending, preparing, delivering, delivered
  deliveryAddress: {
    street: "Av. Providencia 123",
    coordinates: { lat: -33.4489, lng: -70.6693 }
  },
  createdAt: timestamp,
  estimatedDelivery: timestamp
}
```

## 🎨 Diseño UI/UX

### Paleta de Colores
- **Primario**: #FFD700 (Amarillo)
- **Secundario**: #FF6B35 (Naranja)
- **Acento**: #4ECDC4 (Turquesa)
- **Neutro**: #2C3E50 (Azul Oscuro)
- **Fondo**: #F8F9FA (Gris Claro)

### Principios de Diseño
- 🎯 **Simplicidad**: Interfaz limpia y fácil de usar
- 🚀 **Velocidad**: Carga rápida y navegación fluida
- 📱 **Responsive**: Adaptable a diferentes tamaños de pantalla
- ♿ **Accesibilidad**: Inclusivo para todos los usuarios
- 🎨 **Consistencia**: Diseño coherente en toda la app

## 📸 Mockups de Pantallas

<div align="center">
  <img src="https://via.placeholder.com/300x600/ffd700/ffffff?text=Pantalla+Principal" alt="Home Screen" width="150" />
  <img src="https://via.placeholder.com/300x600/ffd700/ffffff?text=Restaurantes" alt="Restaurants" width="150" />
  <img src="https://via.placeholder.com/300x600/ffd700/ffffff?text=Carrito" alt="Cart" width="150" />
  <img src="https://via.placeholder.com/300x600/ffd700/ffffff?text=Seguimiento" alt="Tracking" width="150" />
</div>

## 🧪 Testing Strategy

### Unit Tests
- Componentes React Native
- Hooks personalizados
- Utilidades y helpers
- Servicios de API

### Integration Tests
- Flujo de autenticación
- Proceso de pedido completo
- Integración con mapas
- Sistema de pagos

### E2E Tests
- Flujos completos de usuario
- Navegación entre pantallas
- Interacciones con APIs externas

## 🚀 Despliegue

### App Store / Google Play
- Configuración de Expo Application Services
- Certificados y provisioning profiles
- Configuración de builds automáticos
- Proceso de review y publicación

### Firebase
- Configuración de proyectos
- Reglas de seguridad
- Monitoreo y analytics
- Backup y recuperación

## 📈 Métricas y Analytics

- 📊 Usuarios activos diarios/mensuales
- 🛒 Tasa de conversión de pedidos
- ⏱️ Tiempo promedio de entrega
- ⭐ Calificaciones promedio
- 💰 Valor promedio de pedido
- 📱 Retención de usuarios

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
  <img src="https://img.shields.io/badge/Made%20with%20%E2%9D%A4%EF%B8%8F-Santiago%20de%20Chile-ffd700?style=for-the-badge" alt="Made with love" />
</div> 