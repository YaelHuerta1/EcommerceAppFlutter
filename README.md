# EcommerceAppFlutter

Aplicación móvil de comercio electrónico desarrollada con Flutter para la venta de productos de calzado y moda urbana. El proyecto combina una experiencia visual moderna, navegación por pantallas, dashboard con menú lateral, catálogo de productos y detalle de producto, con una estética inspirada en tiendas de e-commerce premium.

## Descripción general

La app está diseñada como una tienda digital con flujo de usuario típico:

- Splash screen animada al iniciar
- Pantalla de login y registro
- Dashboard principal con navegación por secciones
- Catálogo de productos con carousel y categorías
- Vista detallada de cada artículo
- Perfil de usuario y acceso a menú lateral
- Uso de assets gráficos, animaciones y tipografía personalizada

El proyecto está enfocado en la capa de UI/UX, demostrando buenas prácticas de composición de widgets, routing y organización de recursos.

## Stack tecnológico

- Flutter SDK
- Dart
- Material Design
- Assets locales (imágenes, SVG, animaciones Lottie)
- Paquetes de terceros para UI y utilidades

## Arquitectura del proyecto

La estructura del repositorio sigue una organización simple y modular para aplicaciones Flutter en etapa de prototipo/desarrollo:

```text
EcommerceAppFlutter/
├── android/                 # Configuración nativa de Android
├── ios/                     # Configuración nativa de iOS
├── assets/
│   ├── images/              # Imágenes del catálogo y de fondo
│   ├── icons/               # Íconos y assets vectoriales
│   ├── anims/               # Animaciones Lottie
│   └── fonts/               # Tipografías personalizadas
├── lib/
│   ├── components/          # Widgets reutilizables (botones, inputs, cards, nav)
│   ├── constants/           # Colores, imágenes, datos dummy
│   ├── models/              # Modelos de dominio (Product)
│   ├── screens/             # Pantallas principales de la app
│   ├── main.dart            # Punto de entrada de la aplicación
│   ├── route_generator.dart # Manejo de rutas/navegación
│   └── ...
├── test/                    # Pruebas (si se agregan)
├── analysis_options.yaml    # Reglas de linting
├── pubspec.yaml             # Dependencias y configuración del proyecto
├── pubspec.lock             # Lock file
├── .gitignore
└── README.md
```

### Principios de organización

- `main.dart`: configura `MaterialApp`, tema general y ruta inicial.
- `route_generator.dart`: centraliza la navegación entre pantallas.
- `screens/`: alberga las vistas principales (login, splash, dashboard, perfil, detalle del producto).
- `components/`: widgets UI reutilizables para mantener consistencia visual.
- `constants/`: valores compartidos como colores, assets y datos de ejemplo.
- `models/`: modelos de negocio, destacando `Product`.

## Funcionalidades principales

- Pantalla de bienvenida con animación Lottie
- Inicio de sesión y registro visualmente estilizado
- Menú lateral tipo dashboard con navegación de secciones
- Catálogo de productos con carrusel horizontal
- Selección de categorías
- Tarjetas de productos con precio, valoración y acción de compra
- Vista de detalle de producto con imágenes, descripción y colores disponibles
- Perfil del usuario y diseño adaptable a diferentes tamaños de pantalla

## Modelo de datos

El proyecto define un modelo central llamado `Product`, el cual encapsula la información de los artículos vendidos:

- `name`
- `brand`
- `description`
- `price`
- `rating`
- `productColors`
- `productImages`

Este diseño permite construir la UI de forma dinámica a partir de datos de ejemplo, y facilita la expansión hacia una API real o una base de datos en el futuro.

## Paquetes principales

El archivo `pubspec.yaml` incluye las siguientes dependencias relevantes:

- `flutter` / `dart`: base del proyecto
- `cupertino_icons`: íconos del sistema iOS
- `google_fonts`: tipografía moderna y personalizable
- `flutter_svg`: renderización de SVG para iconos/vectoriales
- `lottie`: animaciones de alta calidad
- `velocity_x`: utilidades rápidas para layouts y estilos en UI
- `dots_indicator`: indicador de páginas para carousels
- `font_awesome_flutter`: iconos de Font Awesome
- `file`: soporte para acceso a archivos

Además, incluye `flutter_lints` como dependencia de desarrollo para mantener un código limpio y consistente.

## Tema visual

La app usa un esquema visual sólido y moderno:

- fondo blanco con acentos oscuros
- paleta basada en tonos morados, grises y azul profundo
- tipografía personalizada `Gilroy`
- componentes con bordes redondeados, sombras suaves y tarjetas elevadas
- una estética orientada a tiendas premium de sneakers o accesorios de moda

## Requisitos previos

Antes de ejecutar la app asegúrate de tener instalado:

- Flutter SDK (versión compatible con el `pubspec.yaml`)
- Dart SDK
- Android Studio o VS Code con extensiones de Flutter
- Un emulador o dispositivo físico conectado

## Cómo ejecutar el proyecto

1. Clona el repositorio:

```bash
git clone https://github.com/YaelHuerta1/EcommerceAppFlutter.git
cd EcommerceAppFlutter
```

2. Instala las dependencias:

```bash
flutter pub get
```

3. Ejecuta la aplicación:

```bash
flutter run
```

4. Si deseas abrirlo en un dispositivo o emulador específico:

```bash
flutter devices
flutter run -d <device_id>
```

## Comandos útiles

- Verificar dependencias:

```bash
flutter doctor
```

- Ejecutar pruebas:

```bash
flutter test
```

- Generar build de producción (Android):

```bash
flutter build apk
```

- Generar build de producción (iOS, requiere macOS):

```bash
flutter build ios
```

## Observaciones de desarrollo

Este repositorio funciona como una base sólida para una app de e-commerce con enfoque visual y experiencia de usuario. Actualmente tiene una estructura orientada a prototipo/UI, pero puede escalarse fácilmente hacia:

- consumo de API REST
- autenticación real
- carrito de compras persistente
- gestión de órdenes
- pagos integrados
- almacenamiento local con SQLite/SharedPreferences/Hive
- arquitectura más robusta como Bloc, Provider, Riverpod o GetX

## Contribución

Si deseas colaborar en el proyecto, puedes:

- mejorar la estructura de carpetas
- agregar autentización real
- conectar la UI con una API de productos
- implementar carrito y checkout
- añadir pruebas unitarias e integración

## Licencia

Este proyecto no especifica una licencia en el archivo de configuración del repositorio, por lo que se recomienda revisar el estado legal antes de reutilizarlo en producción o distribuirlo públicamente.

## Autor

Proyecto desarrollado por YaelHuerta1.

---

Si quieres, puedo ayudarte también a:

- generar una versión más detallada del README con screenshots
- convertir la app a una arquitectura MVC/Bloc
- documentar cada pantalla del proyecto
- crear un README con formato más comercial para GitHub
