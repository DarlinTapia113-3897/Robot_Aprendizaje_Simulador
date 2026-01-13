# Robot_Aprendizaje_Simulador
Swarm Analyzer Elite es un simulador de enjambres basado en IA con Q-Learning. Los agentes inteligentes con habilidades únicas (velocidad, memoria, exploración) aprenden en tiempo real a resolver laberintos dinámicos. Incluye un dashboard con GPS, ranking de eficiencia y telemetría avanzada mediante Tailwind CSS y JavaScript.

📡 Swarm Analyzer Elite
Swarm Analyzer Elite es una plataforma de simulación interactiva basada en la web donde múltiples agentes inteligentes (robots) compiten y colaboran para resolver laberintos generados proceduralmente. El proyecto utiliza Aprendizaje por Refuerzo (Q-Learning) para que los robots "aprendan" el camino óptimo hacia la meta.

🚀 Características Principales
IA con Q-Learning: Cada robot posee una tabla de memoria (Q-Table) que se actualiza en tiempo real, optimizando su toma de decisiones según las recompensas recibidas.

Sistema de Habilidades: Puedes desplegar agentes con diferentes especialidades que afectan su comportamiento:

⚡ Velocidad: Se mueve el doble de rápido por turno.

👁️ Percepción: Penalización reducida al chocar con paredes.

🗺️ Explorador: Recibe bonificaciones altas por descubrir celdas nuevas.

🧠 Memoria: Posee una tasa de aprendizaje (LearningRate) superior para adaptarse rápido.

Dashboard en Tiempo Real: Monitoreo de posición GPS, logs de misión y porcentaje de exploración del mapa.

Ranking de Eficiencia: Clasificación automática de los robots basada en su promedio de pasos para alcanzar el éxito.

🛠️ Tecnologías Utilizadas
HTML5 & CSS3: Estructura y diseño con animaciones personalizadas.

Tailwind CSS: Framework de utilidades para un diseño moderno y responsivo.

JavaScript (Vanilla): Lógica del motor de simulación, algoritmos de IA y manipulación del DOM.

Google Fonts: Tipografía "Quicksand" para una interfaz amigable.

🕹️ Instrucciones de Uso
Configuración del Agente: Selecciona una habilidad en el menú "Centro de Mando".

Despliegue: Haz clic en "Desplegar Agente" para añadir un robot al punto de inicio (esquina superior izquierda).

Ejecución: Pulsa "Iniciar" para ver a los robots explorar.

Optimización: Ajusta el "Velocidad del Motor" para acelerar la simulación o crea un "Nuevo Mapa" para poner a prueba la adaptabilidad de la IA.

🧠 Lógica de la IA (Q-Learning)
El aprendizaje se basa en la ecuación de Bellman simplificada, donde el valor de una acción en un estado (s,a) se actualiza de la siguiente manera:

Q(s,a)←Q(s,a)+α[r+γmaxQ(s 
′
 ,a 
′
 )−Q(s,a)]
Exploración vs. Explotación: Los robots usan una estrategia Epsilon-Greedy (ϵ=0.15) para decidir si explorar rutas nuevas o usar el conocimiento ya adquirido.

Recompensas: Los agentes reciben +100 al llegar a la meta (🏆) y penalizaciones pequeñas por cada paso o choque.

📂 Estructura del Código
class Robot: Define las propiedades físicas, la lógica de movimiento y el cerebro de aprendizaje de cada agente.

initMaze(): Genera laberintos aleatorios asegurando que la meta sea alcanzable.

gameLoop(): El motor que coordina los turnos de todos los robots activos.

¿Te gustaría que añada una sección sobre cómo personalizar las recompensas de la IA o cómo instalarlo localmente?

