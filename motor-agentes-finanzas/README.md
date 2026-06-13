# Motor de Agentes Financieros 🤖💰

Motor de análisis financiero impulsado por la API de Groq, con múltiples agentes especializados.

## Estructura del Proyecto

```
motor-agentes-finanzas/
├── src/
│   └── agentes/
│       ├── tecnico.js       # Análisis técnico de mercados
│       ├── sentimiento.js   # Análisis de sentimiento
│       └── manager.js       # Coordinador de análisis
├── .env                      # Variables de entorno
├── .gitignore               # Archivos ignorados por Git
├── server.js                # Servidor Express principal
└── package.json             # Dependencias del proyecto
```

## Instalación

1. **Instalar dependencias**
   ```bash
   cd motor-agentes-finanzas
   npm install
   ```

2. **Configurar variables de entorno**
   ```bash
   # Editar .env y agregar tu API key de Groq
   GROQ_API_KEY=tu_api_key_aquí
   PORT=3000
   ```

## Uso

### Iniciar servidor
```bash
npm start
```

### Modo desarrollo (con nodemon)
```bash
npm run dev
```

## Agentes Disponibles

### 🔍 Agente Técnico
Realiza análisis técnico de activos financieros:
- Tendencias del mercado
- Soportes y resistencias
- Señales de entrada/salida

### 📊 Agente Sentimiento
Analiza el sentimiento del mercado:
- Análisis de noticias financieras
- Sentimiento positivo/negativo
- Confianza de predicciones

### 🎯 Agente Manager
Coordina los análisis de otros agentes:
- Síntesis de información
- Recomendaciones consolidadas
- Toma de decisiones

## Dependencias

- **express**: Framework web minimalista
- **cors**: Manejo de CORS
- **dotenv**: Gestión de variables de entorno
- **groq-sdk**: SDK oficial de Groq
- **nodemon**: Reinicio automático en desarrollo

## API Reference

### GET `/`
Estado del servidor

**Response:**
```json
{
  "mensaje": "Motor de Agentes Financieros activo",
  "version": "1.0.0"
}
```

## Ejemplos de Uso

```javascript
const AgenteTecnico = require('./src/agentes/tecnico');
const agente = new AgenteTecnico();

const analisis = await agente.analizarTendencia('AAPL', {
  precio_actual: 150.25,
  precio_apertura: 149.50,
  precio_maximo: 151.00
});

console.log(analisis);
```

## Configuración de Groq

Para obtener tu API key de Groq:
1. Visita [console.groq.com](https://console.groq.com)
2. Crea una cuenta
3. Genera una nueva API key
4. Pégala en el archivo `.env`

## Próximas Mejoras

- [ ] Base de datos para historial de análisis
- [ ] Webhooks para alertas en tiempo real
- [ ] Dashboard web de visualización
- [ ] Integración con APIs de mercado
- [ ] Pruebas unitarias
- [ ] Documentación de API con Swagger

## Licencia

ISC
