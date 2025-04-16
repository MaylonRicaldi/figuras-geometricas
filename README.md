# Figuras Geometricas
## Desarrollador
| Apellidos y nombres |
| --- |
| Ricaldi Solis Maylon Amilcar|

Este archivo contiene una descripción de los cambios realizados en el código Python para cumplir con las buenas prácticas de PEP 8 y mejorar su legibilidad y estructura.

## Cambios Realizados

### 1. **C0103: Module name "FiguraGeometrica" doesn't conform to snake_case naming style**
- **Descripción:**  
El nombre del archivo `FiguraGeometrica.py` no sigue el estilo de nomenclatura recomendado por PEP 8. Según las normas de PEP 8, los nombres de archivo deben estar en minúsculas y usar guiones bajos para separar palabras (estilo `snake_case`).
  
- **Corrección:**  
Se renombró el archivo `FiguraGeometrica.py` a `figura_geometrica.py` para cumplir con la convención de nomenclatura de PEP 8.

### 2. **C0114: Missing module docstring**
- **Descripción:**  
El módulo no tiene una docstring al inicio, lo que es necesario para proporcionar una descripción general de lo que hace el archivo.
  
- **Corrección:**  
Se agregó una docstring al inicio del archivo para describir brevemente su propósito:
  ```python
  """Este módulo define figuras geométricas básicas y calcula sus áreas."""
  
### 3. **W0107: Unnecessary pass statement**
- **Descripción:**  
La sentencia `pass` en el método `calcular_area` de la clase abstracta `FiguraGeometrica` es innecesaria. El método ya está marcado como `@abstractmethod`, lo que significa que no requiere una implementación en la clase base, ya que se espera que sea implementado por las subclases.

- **Corrección:**  
Se eliminó la sentencia `pass` en el método abstracto `calcular_area`, ya que no es necesaria. El código corregido es el siguiente:
  ```python
  @abstractmethod
  def calcular_area(self):
      """Calcula el área de la figura geométrica."""
      raise NotImplementedError("Este método debe ser implementado por una subclase.")
