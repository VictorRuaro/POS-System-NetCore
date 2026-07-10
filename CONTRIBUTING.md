# Guía de Contribución

Gracias por tu interés en contribuir a **POS System - .NET Core**.

## 📋 Antes de Comenzar

1. Fork el repositorio
2. Clona tu fork: `git clone https://github.com/tu-usuario/POS-System-NetCore.git`
3. Crea una rama: `git checkout -b feature/nombre-descriptivo`

## 🎯 Proceso de Contribución

### 1. Hacer Cambios

- Sigue las Convenciones de Código
- Escriba pruebas para nuevas características
- Ejecuta los tests: `dotnet test`

### 2. Commit y Push

```bash
git commit -m "feat: Descripción de la característica"
git push origin feature/nombre-descriptivo
```

### 3. Crear Pull Request

- Proporciona una descripción clara de los cambios
- Vincula issues relacionados
- Espera revisión del equipo

## 📝 Convenciones de Código

### Naming Conventions

- Public members: **PascalCase**
- Private members: **camelCase**
- Constants: **PascalCase**

### Async/Await

- Usar async por defecto para I/O operations
- Métodos async deben terminar con "Async"

### SOLID Principles

- Inyección de Dependencias
- Single Responsibility
- Open/Closed Principle

## 🧪 Testing

```bash
# Ejecutar todos los tests
dotnet test

# Con coverage
dotnet test /p:CollectCoverage=true /p:CoverageFormat=opencover
```

## 🚀 Ramas

```
main/           - Producción (releases)
  ├─ develop/  - Desarrollo
      ├─ feature/...
      ├─ bugfix/...
      └─ hotfix/...
```

## 📌 Tipos de Commits

- **feat**: Nueva característica
- **fix**: Corrección de bug
- **docs**: Cambios en documentación
- **style**: Cambios de formato
- **refactor**: Refactorización
- **test**: Agregar tests
- **chore**: Cambios en build
- **perf**: Mejoras de rendimiento

## ✅ Checklist Previo a PR

- [ ] El código compila sin errores
- [ ] Todos los tests pasan
- [ ] Código tiene XML documentation
- [ ] >80% de coverage en tests
- [ ] Mensaje de commit descriptivo
- [ ] Rama actualizada con develop

---

¡Gracias por contribuir! 🎉
