# 🛒 POS System - .NET Core

Sistema de Punto de Venta (POS) completo construido con **.NET Core 8.0**, siguiendo arquitectura **Clean Architecture** y principios **SOLID**.

## 📋 Descripción del Proyecto

Aplicación empresarial de punto de venta con capacidades completas de:
- 🛍️ Gestión de ventas en tiempo real
- 📦 Control de inventario multi-almacén
- 💳 Procesamiento de múltiples métodos de pago
- 📊 Reportes y análisis avanzados
- 👥 Gestión de usuarios y roles
- 🔐 Autenticación y autorización segura
- 📱 API RESTful y aplicación web

## 🚀 Stack Tecnológico

### Backend
- **.NET Core 8.0 LTS**
- **Entity Framework Core 8.0**
- **ASP.NET Core Web API**
- **SQL Server / PostgreSQL**
- **MediatR** (CQRS Pattern)
- **AutoMapper**
- **FluentValidation**

### Frontend
- **Angular 17+** o **React 18+**
- **Material Design / Bootstrap**
- **TypeScript**
- **RxJS**

### Infrastructure
- **Docker & Docker Compose**
- **Kubernetes** (escalabilidad)
- **Redis** (caché)
- **RabbitMQ** (message queue)
- **ElasticSearch** (búsqueda)
- **Serilog** (logging)

### DevOps
- **GitHub Actions** (CI/CD)
- **Azure DevOps** (opcional)
- **SQL Server Management Studio**

## 📁 Estructura del Proyecto

```
POS-System-NetCore/
├── src/
│   ├── POS.Domain/                 # Entidades y reglas de negocio
│   ├── POS.Application/            # Servicios de aplicación (CQRS)
│   ├── POS.Infrastructure/         # Implementación de repositorios, EF Core
│   ├── POS.Presentation/           # API Controllers
│   └── POS.Tests/                  # Tests unitarios e integración
├── docker/
│   ├── Dockerfile
│   ├── docker-compose.yml
│   └── docker-compose.prod.yml
├── database/
│   ├── migrations/
│   ├── seeds/
│   └── schema.sql
├── .github/
│   └── workflows/
│       ├── build.yml
│       ├── test.yml
│       └── deploy.yml
├── docs/
│   ├── ROADMAP.md
│   ├── ARCHITECTURE.md
│   └── API.md
└── README.md
```

## 🎯 Fases del Desarrollo

### ✅ Fase 1: Preparación y Arquitectura (Semanas 1-4)
- Configuración del proyecto base
- Diseño de base de datos
- Setup de infraestructura y DevOps
- Framework core y librerías

### 🔒 Fase 2: Autenticación y Seguridad (Semanas 5-8)
- Sistema de autenticación JWT
- Roles y permisos (RBAC)
- Auditoría y logging
- 2FA

### 🛒 Fase 3: Módulos Core de Negocio (Semanas 9-16)
- Gestión de productos
- Control de inventario
- Punto de venta (POS)
- Facturación
- Gestión de clientes

### 📊 Fase 4: Reportes y Análisis (Semanas 17-20)
- Dashboard ejecutivo
- Reportes detallados
- Business Intelligence
- Análisis de datos

### 🔧 Fase 5: Integraciones y Optimización (Semanas 21-24)
- Integraciones externas (Stripe, PayPal)
- Sincronización multi-sucursal
- Optimización de performance
- Testing completo

### 🚀 Fase 6: Deployment (Semanas 25-26)
- Preparación de producción
- Go-live
- Soporte post-lanzamiento

## 📖 Documentación

- [ROADMAP.md](./ROADMAP.md) - Roadmap detallado de 26 semanas
- [CONTRIBUTING.md](./CONTRIBUTING.md) - Guía de contribución
- [CHANGELOG.md](./CHANGELOG.md) - Historial de cambios

## 🛠️ Requisitos Previos

- **.NET SDK 8.0+** - [Descargar](https://dotnet.microsoft.com/download)
- **Docker & Docker Compose** - [Descargar](https://www.docker.com/)
- **SQL Server 2022+** o **PostgreSQL 14+**
- **Git** - [Descargar](https://git-scm.com/)
- **Node.js 18+** (para frontend)

## ⚡ Quick Start

### 1. Clonar el repositorio
```bash
git clone https://github.com/VictorRuaro/POS-System-NetCore.git
cd POS-System-NetCore
```

### 2. Configurar el ambiente
```bash
# Copiar archivo de configuración
cp .env.example .env

# Restaurar dependencias
dotnet restore
```

### 3. Ejecutar con Docker
```bash
# Iniciar servicios (Base de datos, Redis, etc.)
docker-compose up -d

# Ejecutar migrations
dotnet ef database update

# Iniciar la aplicación
dotnet run --project src/POS.Presentation
```

### 4. Acceder a la aplicación
- **API**: http://localhost:5000
- **Swagger**: http://localhost:5000/swagger
- **Frontend**: http://localhost:4200

## 🔑 Credenciales por Defecto

```
Email: admin@pos-system.com
Password: Admin@123456
```

⚠️ **Cambiar credenciales en producción**

## 📊 Base de Datos

### Crear BD desde migrations:
```bash
dotnet ef database update -p src/POS.Infrastructure
```

### Crear BD desde script:
```bash
sqlcmd -S localhost -U sa -P YourPassword -i database/schema.sql
```

## 🧪 Testing

```bash
# Ejecutar todos los tests
dotnet test

# Con coverage
dotnet test /p:CollectCoverage=true /p:CoverageFormat=opencover

# Tests específicos
dotnet test --filter "Category=Unit"
```

## 📝 Convenciones de Código

- **NamingConventions**: PascalCase para public, camelCase para private
- **Async/Await**: Usar async por defecto para I/O operations
- **SOLID Principles**: Inyección de dependencias, single responsibility
- **Comments**: XML documentation para métodos públicos

## 🚀 CI/CD Pipeline

El proyecto cuenta con GitHub Actions configurado para:

1. **Build**: Compilar proyecto
2. **Test**: Ejecutar test suite
3. **Deploy**: Desplegar a staging y production

Ver `.github/workflows` para más detalles.

## 🐛 Reporting Issues

Si encuentras un bug, crea un issue en:
https://github.com/VictorRuaro/POS-System-NetCore/issues

Incluye:
- Descripción clara del problema
- Pasos para reproducir
- Comportamiento esperado
- Comportamiento actual
- Environment (OS, .NET version, etc.)

## 🤝 Contributing

Las contribuciones son bienvenidas. Por favor:

1. Fork el repositorio
2. Crea una rama: `git checkout -b feature/amazing-feature`
3. Commit tus cambios: `git commit -m 'Add amazing feature'`
4. Push a la rama: `git push origin feature/amazing-feature`
5. Abre un Pull Request

Ver [CONTRIBUTING.md](./CONTRIBUTING.md) para más detalles.

## 📚 Recursos Útiles

- [.NET Core Documentation](https://docs.microsoft.com/dotnet/)
- [Entity Framework Core](https://docs.microsoft.com/ef/core/)
- [Clean Architecture](https://blog.cleancoder.com/uncle-bob/2012/08/13/the-clean-architecture.html)
- [SOLID Principles](https://en.wikipedia.org/wiki/SOLID)
- [Microservices Pattern](https://microservices.io/)

## 📄 Licencia

Este proyecto está bajo licencia **MIT** - Ver [LICENSE](LICENSE) para detalles.

## 👨‍💻 Autor

**Victor Ruaro**
- GitHub: [@VictorRuaro](https://github.com/VictorRuaro)

## 🙏 Agradecimientos

Agradecemos a:
- La comunidad de .NET Core
- Contribuidores del proyecto
- Usuarios que reportan bugs

## 📞 Soporte

Para soporte:
- 📧 Issues: GitHub Issues
- 📖 Documentación: [Wiki](https://github.com/VictorRuaro/POS-System-NetCore/wiki)

---

**Última actualización**: 2026-07-10
**Versión**: 1.0.0 (En desarrollo)

Hecho con ❤️ por Victor Ruaro
