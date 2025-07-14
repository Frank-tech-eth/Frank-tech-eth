# 🔴 NFT Marketplace - Web3 Application

<div align="center">
  <img src="https://img.shields.io/badge/Status-Completado-ff0000?style=for-the-badge" alt="Status" />
  <img src="https://img.shields.io/badge/Solidity-363636?style=for-the-badge&logo=solidity&logoColor=white" alt="Solidity" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/IPFS-65C2CB?style=for-the-badge&logo=ipfs&logoColor=white" alt="IPFS" />
</div>

## 📋 Descripción

Marketplace completo de NFTs que permite a los usuarios crear, comprar, vender y coleccionar tokens no fungibles. Incluye minting de NFTs, marketplace de trading, y sistema de royalties para creadores.

## ✨ Características

- 🎨 **Minting de NFTs**: Crear tokens únicos con metadatos
- 🛒 **Marketplace**: Comprar y vender NFTs con ETH
- 💰 **Sistema de Royalties**: Pagos automáticos a creadores
- 🔐 **Smart Contracts Auditados**: Seguridad garantizada
- 📱 **Interfaz Web3**: Conexión con wallets populares
- 🖼️ **Almacenamiento IPFS**: Metadatos descentralizados
- 📊 **Analytics**: Estadísticas de ventas y tendencias
- 🎯 **Colecciones**: Organización por categorías

## 🛠️ Tecnologías Utilizadas

### Backend
- **Python 3.11** - Lenguaje de programación
- **FastAPI** - Framework web moderno y rápido
- **SQLAlchemy** - ORM para base de datos
- **PostgreSQL** - Base de datos relacional
- **Pydantic** - Validación de datos
- **JWT** - Autenticación con tokens

### DevOps
- **Docker** - Contenedores
- **Docker Compose** - Orquestación de contenedores
- **Pytest** - Framework de testing
- **Alembic** - Migraciones de base de datos

## 🚀 Instalación

```bash
# Clonar el repositorio
git clone https://github.com/tu-usuario/proyecto-rojo.git
cd proyecto-rojo

# Usando Docker (recomendado)
docker-compose up -d

# O instalación local
python -m venv venv
source venv/bin/activate  # En Windows: venv\Scripts\activate
pip install -r requirements.txt

# Configurar variables de entorno
cp .env.example .env
# Editar .env con tus credenciales

# Ejecutar migraciones
alembic upgrade head

# Ejecutar la aplicación
uvicorn main:app --reload
```

## 📖 Documentación de la API

Una vez ejecutada la aplicación, puedes acceder a:

- **Swagger UI**: http://localhost:8000/docs
- **ReDoc**: http://localhost:8000/redoc
- **OpenAPI JSON**: http://localhost:8000/openapi.json

## 🔧 Endpoints Principales

### Autenticación
- `POST /auth/login` - Iniciar sesión
- `POST /auth/register` - Registrar usuario
- `POST /auth/refresh` - Renovar token

### Productos
- `GET /products` - Listar productos
- `POST /products` - Crear producto
- `GET /products/{id}` - Obtener producto
- `PUT /products/{id}` - Actualizar producto
- `DELETE /products/{id}` - Eliminar producto

### Inventario
- `GET /inventory` - Estado del inventario
- `POST /inventory/move` - Mover stock
- `GET /inventory/history` - Historial de movimientos

## 📊 Estructura de la Base de Datos

```sql
-- Tabla de productos
CREATE TABLE products (
    id SERIAL PRIMARY KEY,
    name VARCHAR(255) NOT NULL,
    description TEXT,
    price DECIMAL(10,2) NOT NULL,
    stock_quantity INTEGER DEFAULT 0,
    category_id INTEGER REFERENCES categories(id),
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Tabla de categorías
CREATE TABLE categories (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    description TEXT
);

-- Tabla de movimientos de inventario
CREATE TABLE inventory_movements (
    id SERIAL PRIMARY KEY,
    product_id INTEGER REFERENCES products(id),
    quantity INTEGER NOT NULL,
    movement_type VARCHAR(20) NOT NULL, -- 'IN' o 'OUT'
    reason TEXT,
    created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## 🧪 Testing

```bash
# Ejecutar todos los tests
pytest

# Ejecutar tests con coverage
pytest --cov=app tests/

# Ejecutar tests específicos
pytest tests/test_products.py
```

## 📸 Capturas de Pantalla

<div align="center">
  <img src="https://via.placeholder.com/800x400/ff0000/ffffff?text=Swagger+Documentation" alt="Swagger" width="400" />
  <img src="https://via.placeholder.com/800x400/ff0000/ffffff?text=API+Response" alt="API Response" width="400" />
</div>

## 🚀 Despliegue

### Heroku
```bash
# Configurar variables de entorno en Heroku
heroku config:set DATABASE_URL=postgresql://...

# Desplegar
git push heroku main
```

### Docker
```bash
# Construir imagen
docker build -t proyecto-rojo .

# Ejecutar contenedor
docker run -p 8000:8000 proyecto-rojo
```

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
  <img src="https://img.shields.io/badge/Made%20with%20%E2%9D%A4%EF%B8%8F-Santiago%20de%20Chile-ff0000?style=for-the-badge" alt="Made with love" />
</div> 