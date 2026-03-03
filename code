using System;

class Program
{
    static void Main(string[] args)
    {
        // 🔹 Entradas
        Console.Write("Ingrese el nombre del jugador: ");
        string nombre = Console.ReadLine();

        Console.Write("Ingrese el puntaje: ");
        int puntaje = int.Parse(Console.ReadLine());

        Console.Write("Ingrese victorias consecutivas: ");
        int victoriasConsecutivas = int.Parse(Console.ReadLine());

        Console.Write("Tipo de cuenta (free/premium): ");
        string tipoCuenta = Console.ReadLine().ToLower();

        Console.Write("¿Es evento especial? (si/no): ");
        string esEventoEspecial = Console.ReadLine().ToLower();

        // 🔹 Proceso - Clasificación
        string rango;
        decimal recompensa;

        if (puntaje >= 2000 && victoriasConsecutivas >= 5)
        {
            rango = "Diamante";
            recompensa = 500;
        }
        else if (puntaje >= 1000 || victoriasConsecutivas >= 3)
        {
            rango = "Oro";
            recompensa = 300;
        }
        else
        {
            rango = "Plata";
            recompensa = 100;
        }

        // 🔹 Bonificación premium
        if (tipoCuenta == "premium" && puntaje >= 1500)
        {
            recompensa += recompensa * 0.20m; // +20%
        }

        // 🔹 Evento especial o racha alta
        if (esEventoEspecial == "si" || victoriasConsecutivas >= 7)
        {
            recompensa *= 2;
        }

        // 🔹 Mensaje motivacional
        string mensaje = $"¡Excelente trabajo {nombre}! Sigue mejorando tu rango.";

        // 🔹 Salidas
        Console.WriteLine("\n===== RESULTADOS =====");
        Console.WriteLine($"Jugador: {nombre}");
        Console.WriteLine($"Rango asignado: {rango}");
        Console.WriteLine($"Monedas obtenidas: {recompensa}");
        Console.WriteLine(mensaje);
    }
}
