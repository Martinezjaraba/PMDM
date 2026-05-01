# 📱 Curso: Programación Multimedia y Dispositivos Móviles (2º DAM - Aragón)

## 🧭 Contexto del módulo

Repositorio oficial del curso para el módulo de **Programación Multimedia y Dispositivos Móviles** (CFGS DAM, Aragón).

* 🗓️ Periodo: mediados de septiembre → finales de febrero
* ⏱️ Carga: 6 h/semana (~120 horas reales)
* 🧪 Enfoque: 100% práctico + aprendizaje basado en proyectos
* 🧰 Stack: Kotlin + Android moderno + Jetpack Compose

---

## 🎯 Resultados de aprendizaje (adaptados)

Al finalizar el módulo el alumnado será capaz de:

* Desarrollar apps Android funcionales en Kotlin
* Diseñar interfaces modernas con Compose
* Gestionar navegación entre pantallas
* Consumir APIs REST
* Persistir datos localmente
* Aplicar arquitectura básica (MVVM)

---

## 📅 Temporalización realista

| Bloque         | Horas  | Semanas |
| -------------- | ------ | ------- |
| Kotlin básico  | 10-12h | 2       |
| Intro Android  | 10h    | 2       |
| UI Compose     | 25h    | 4       |
| Navegación     | 10h    | 2       |
| Arquitectura   | 15h    | 3       |
| APIs           | 15h    | 3       |
| Persistencia   | 10h    | 2       |
| Proyecto final | 25-30h | resto   |

---

## 🗂️ Estructura del repositorio

```
curso/
ejercicios/
soluciones/
proyecto-base/
```

---

## 🧪 Sistema de evaluación (oficial adaptado)

| Elemento             | Peso |
| -------------------- | ---- |
| Prácticas evaluables | 40%  |
| Proyecto final       | 40%  |
| Pruebas técnicas     | 20%  |

---

## 📊 Rúbricas oficiales simplificadas

### 🧪 Prácticas evaluables

| Criterio         | Excelente (10)            | Aceptable (5)         | Insuficiente (0-4) |
| ---------------- | ------------------------- | --------------------- | ------------------ |
| Funcionalidad    | Completa y sin errores    | Funciona parcialmente | No funciona        |
| Código           | Limpio, modular           | Mejorable             | Caótico            |
| Buenas prácticas | Usa MVVM, estado correcto | Uso parcial           | Incorrecto         |

---

### 🚀 Proyecto final

| Criterio         | Peso | Descripción                     |
| ---------------- | ---- | ------------------------------- |
| Funcionalidad    | 30%  | App completa y estable          |
| Arquitectura     | 20%  | Uso correcto de ViewModel       |
| UI/UX            | 20%  | Interfaz usable                 |
| Persistencia/API | 20%  | Datos gestionados correctamente |
| Código           | 10%  | Legibilidad y estructura        |

---

## 🧩 Ejercicios evaluables (DETALLADOS)

### 🟢 1. Kotlin (10%)

Gestor de tareas en consola

* CRUD completo
* Uso de listas
* Funciones

---

### 📱 2. Compose (15%)

App contador avanzado

* Estado
* UI reactiva

---

### 🔀 3. Navegación (15%)

App lista + detalle

---

### 🌐 4. API (20%)

App consumo REST

* Retrofit
* Loading + errores

---

### 💾 5. Persistencia (10%)

App notas con Room

---

### 🚀 6. Proyecto final (30%)

Requisitos obligatorios:

* 3+ pantallas
* Navegación
* API o Room
* MVVM básico

---

## 🏗️ Proyecto base (starter listo)

### 📁 Estructura

```
app/
 ├── data/
 │   ├── remote/
 │   └── local/
 │
 ├── domain/
 │
 ├── ui/
 │   ├── screens/
 │   └── components/
 │
 ├── navigation/
 │
 └── viewmodel/
```

---

## 🔧 Incluye el starter

✔ Navegación configurada
✔ 2 pantallas
✔ ViewModel
✔ Estado básico

---

## 💻 Ejemplo base

```kotlin
// MainActivity.kt
class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            AppNavigation()
        }
    }
}
```

```kotlin
// Navigation
@Composable
fun AppNavigation() {
    val navController = rememberNavController()

    NavHost(navController, startDestination = "home") {
        composable("home") { HomeScreen(navController) }
        composable("detail") { DetailScreen() }
    }
}
```

```kotlin
// ViewModel
class MainViewModel : ViewModel() {
    var counter by mutableStateOf(0)
        private set

    fun increment() {
        counter++
    }
}
```

---

## 📌 Metodología docente

* Clases prácticas guiadas
* Ejercicios progresivos
* Corrección en vivo
* Uso de Git (branches + PRs)

---

## ⚠️ Normas del curso

* Código limpio obligatorio
* Entregas en fecha
* Uso de repositorio Git

---

## 📬 Soporte

Usar Issues del repositorio para dudas.

---

## 🚀 Recomendación clave

Trabajar SIEMPRE sobre proyectos base. No empezar desde cero en cada práctica.
