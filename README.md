# RankMaste ProyectoIntegrador
Integrante

Diego Andrés Avendaño Zambrano
# Descripción

Programa en C# que evalúa el rendimiento de un jugador según su puntaje, número de victorias consecutivas, tipo de cuenta y eventos especiales. El sistema asigna un rango competitivo y calcula recompensas en monedas virtuales aplicando bonificaciones acumulativas según reglas de negocio.
#  IPO

 ENTRADAS
 | Nombre                | Tipo   | Descripción                         |
| --------------------- | ------ | ----------------------------------- |
| puntaje               | int    | Puntos obtenidos por el jugador     |
| victoriasConsecutivas | int    | Número de partidas ganadas seguidas |
| tipoCuenta            | string | "free" o "premium"                  |
| esEventoEspecial      | string | "si" o "no"                         |

# PROCESO

Clasificación por rendimiento:

Si puntaje ≥ 2000 && victoriasConsecutivas ≥ 5 → Rango Diamante.

Si puntaje ≥ 1000 || victoriasConsecutivas ≥ 3 → Rango Oro.

En otro caso → Rango Plata.

Asignar recompensa base según rango:

Plata → 100 monedas.

Oro → 300 monedas.

Diamante → 500 monedas.

Bonificación por cuenta premium:

Si tipoCuenta == "premium" && puntaje ≥ 1500
→ Se incrementa la recompensa en 20%.

Evento especial o racha alta:

Si esEventoEspecial == "si" || victoriasConsecutivas ≥ 7
→ La recompensa se duplica.

Las reglas pueden cruzarse, por lo que el orden de evaluación influye en el resultado final.


 SALIDAS

Rango asignado.

Total de monedas obtenidas.

Mensaje motivacional para el jugador.

# Tabla de Variables
| Nombre                | Tipo C# | Propósito                   |
| --------------------- | ------- | --------------------------- |
| puntaje               | int     | Puntos ingresados           |
| victoriasConsecutivas | int     | Racha de victorias          |
| tipoCuenta            | string  | Tipo de cuenta del jugador  |
| esEventoEspecial      | string  | Indica si hay evento activo |
| rango                 | string  | Nivel competitivo asignado  |
| recompensa            | decimal | Monedas finales calculadas  |
| mensaje               | string  | Texto mostrado al usuario   |

# Casos de Prueba
Caso 1

Entrada:

puntaje: 2200

victoriasConsecutivas: 6

tipoCuenta: premium

esEventoEspecial: si

Salida esperada:
Rango Diamante con bonificación premium y recompensa duplicada por evento especial.

Caso 2

Entrada:

puntaje: 900

victoriasConsecutivas: 1

tipoCuenta: free

esEventoEspecial: no

Salida esperada:
Rango Plata sin bonificaciones.


