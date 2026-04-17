## 𐙚 ‧₊˚ ⋅ Pagina Web sobre La Cienega de Mallorquín

૮ ˶ᵔ ᵕ ᵔ˶ ა  
#### Esta es una pagina web, que utiliza algunos metodos de **flexbox**, **CSS Grid**, *margin*, *padding* y en general todo lo referenta a modelo de caja de css. Se intenta llevar una buena semantica en el html con el objetivo de emular una buena interfaz de usuario, agradable y landeable.
---

## 𐙚 ‧₊˚ ⋅ Project Overview

Este proyecto tiene las funciones o vistas principales

- Permite llegar a links por medio de un **navbar**
- Se puede ver un **mapa de google maps en tiempo real**
- Tiene las normas básicas de cuidado **en espacios ecologicos**
- Su interfaz es atractiva porqué **tiene animaciones**

---

## 𐙚 ‧₊˚ ⋅ Program Structure

### 📚 

The program includes a list with the following faculties:

- Engineering  
- Languages  
- Legal Sciences  
- Health Sciences  

The user selects one of these options at the beginning of the program.

---

### 👩‍🎓 Students List

An **empty list** called `estudiantes` is used to store student information during the program execution.

All registered students are temporarily stored in this list.

---

### 📄 CSV File Storage

At the end of the program, the student information is stored in a **CSV file named `clientes.csv`**, allowing the data to be saved permanently.

---

## 𐙚 ‧₊˚ ⋅ Functions

### `mostrar()`

This function prints the students stored in the `estudiantes` list.

It helps visualize all registered students during the session.

---

## 𐙚 ‧₊˚ ⋅ Program Flow

1. The program asks the user to **choose a faculty** (from 1 to 4).
2. The selected faculty is displayed.
3. The program enters a **loop**.
4. Inside the loop, the system:
   - Requests student information
   - Stores the data in the `estudiantes` list
5. The loop continues until the user types **`n`** to stop.
6. Finally, the data is **saved into the CSV file**.

---

## 𐙚 ‧₊˚ ⋅ Notes

Even though the requirements may vary in complexity, the program successfully registers multiple students and stores their information efficiently.

---

૮ ˶ᵔ ᵕ ᵔ˶ ა  
*A small console project, but a solid step toward learning data management and file handling in Python.*

```python
cursos = [
    "Facultad de ingeniería",
    "Facultad de idiomas",
    "Facultad de ciencias juridicas",
    "Facultad de ciencias de la salud"
]

estudiantes = []

def interactuar(estudiante):
    if len(estudiante.split(" - ")) == 3:
        print("Admit.ido")
        estudiantes.append(estudiante)
        letra = input("Filtrar por inicial: ")
        if estudiante.startswith(letra):
            print(estudiante)
    else:
        print("Cantidad de valores incorrecta, inténtelo nuevamente")

def mostrar():
    for i in estudiantes:
        print(i)

while True:
    try:
        opcion = int(input("Seleccione un curso (1-4): "))
        if opcion <= 0 or opcion > 4:
            raise IndexError
        break
    except:
        print("Opción inválida")

if 1 <= opcion <= 4:
    print(cursos[opcion-1])

while True:
    interactuar(input("Ingrese nombre - curso - carrera del estudiante: "))
    boton = input("¿Seguir registrando? (s/n): ").lower()
    if boton == 'n':
        mostrar()
        break
f = open("clientes.csv", "w")

for e in estudiantes:
    f.write(e + "\n")

f.close()
```
