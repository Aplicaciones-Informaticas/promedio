def calcular_estadisticas(notas):
    if not notas:
        return "No se ingresaron notas."
    
    promedio = sum(notas) / len(notas)
    nota_max = max(notas)
    nota_min = min(notas)
    
    return f"Promedio: {promedio:.2f}\nNota más alta: {nota_max}\nNota más baja: {nota_min}"

notas = []
while True:
    entrada = input("Ingrese una nota (o 'fin' para terminar): ")
    if entrada.lower() == 'fin':
        break
    try:
        nota = float(entrada)
        if 0 <= nota <= 100:
            notas.append(nota)
        else:
            print("Ingrese una nota válida entre 0 y 100.")
    except ValueError:
        print("Entrada no válida. Intente de nuevo.")

print(calcular_estadisticas(notas))

