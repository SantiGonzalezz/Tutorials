# Visual Basic for Applications

## Índice

1. [Fórmulas](#fórmulas)
   - [Basics](#basic)
   - [String Functions](#string-functions)
   - [Array Functions](#array-functions)
1. [Debug.Print](#debugprint)
1. [Dim](#dim)
1. [Arreglos](#arreglos)
1. [Collections](#collections)
1. [Range](#range)
   - [Propiedades](#propiedades)
   - [Métodos](#métodos)
1. [Condicionales](#condicionales)
   - [If](#if)
   - [Select Case](#select-case)
1. [Estructuras Determinadas](#estructuras-determinadas)
   - [For](#for)
   - [For Each](#for-each)
1. [Estructuras Indeterminadas](#estructuras-indeterminadas)
   - [Do While](#do-while)
   - [Do Until](#do-until)
   - [While](#while)
1. [Funciones](#function)

---

[Índice](#índice)

## Funciones nativas

[Índice](#índice)

### Basics

- `TypeName()`
- `WorksheetFunction.<excel function>()`
- `a Mod b`
  Devuelve el residuo de la división del número a entre el número b
- `Cint (x)`:
  Devuelve el valor x convertido a tipo Integer
- `Cdbl (a)`:
  Devuelve el valor a convertido a tipo Double
- `Cstr (x)`:
  Devuelve el valor x convertido a tipo String
- `CLng (x)`:
  Devuelve el valor x convertido a tipo Long. Long es un entero, puede guardar valores más grandes
- `IsEmpty(y)`
  Revisa si y está vacío
- `IsNull(y)`
  Revisa si y es nulo
- `IsNumeric(y)`
  Revisa si y es un número
- `IsArray(x)`
  Revisa si x es un arreglo

[Índice](#índice)

### String Functions

- `Len (x as String)`:
  Devuelve el número de letras en una cadena de texto x
- `Mid (x as String, y as Long, [z as Long])`:
  Extrae de una cadena de texto x, otra cadena que empieza en la posición y. Se extraen z caracteres
- `Ucase (x as String`:
  Devuelve una cadena de texto x en mayúsculas
- `Lcase (x as String`:
  Devuelve una cadena de texto x en minúsculas
- `InStr ([n as Integer], x as String, a as String)`
  Devuelve la posición de un substring a dentro de x, buscando desde la posición n
- `StrReverse(x as String)`
  Invierte la cadena x. Ej: StrReverse("Hola")=“aloH"
- `Trim(x as String)`
  Quita espacios antes de la primera o después de la última letra de la palabra x. Ej: Trim Uno dos ”)”)==“Uno dos".
- `Replace(x as String, a as String, b as String)`
  Reemplaza un substring a por el substring b dentro de x
- `Left(x as String n as Integer)`
  Devuelve un substring desde el inicio de la cadena hasta la posición n. Igual a IZQUIERDA() de Excel
- `Right(x as String n as Integer)`
  Devuelve un substring desde Len(x) nhasta el final de la cadena. Igual a DERECHA() de Excel

[Índice](#índice)

### Array Functions

- `LBound(Arr)`
  Devuelve el índice en donde irá el primer elemento del arreglo
- `UBound(Arr)`
  Devuelve el índice en donde irá el último elemento del arreglo

---

[Índice](#índice)

## `Debug.Print`

El equivalente a hacer un `print` en consola en python se muestra en la ventana _inmediato_ del editor de VBA

Nota: La ventana inmediato se muestra con `Ctrl + G`

![print](https://i.ibb.co/6Pbmk65/image.png)

---

[Índice](#índice)

## `Dim`

Las variables en VBA no necesitan ser declaradas.

Sin embargo, puede ser de utilidad para variables que solo pueden tener enteros como valor por ejemplo. Ya que si recibe como valor un string `variable = "2"` debido a que declaramos el tipo de valor de la variable, esta convertirá el string en integer.

![dim](https://i.ibb.co/DgXGkDd/image.png)

---

[Índice](#índice)

## Arreglos

Para crear Arrays debemos definir el tipo de valores a almacenar, similar a _NumPy_ donde solo se puede guardar un tipo de dato.

La sintaxis de un arreglo de tamaño fijo es

```VB
Dim <nombre Arreglo>(1 To n) As <Tipo de Dato>
```

La sintaxis de un arreglo de tamaño fijo es

```VB
Dim <nombre Arreglo>() As <Tipo de Dato>
```

Si no se define el tamaño inicial del array podemos cambiar el número de elementos con
`ReDim`

Si queremos cambiar el tamaño de un array que ya tiene un tamaño inicial y valores guardados dentro de este se usa
`ReDim Preserve`

![ReDim](https://i.ibb.co/G0H270F/image.png)

---

[Índice](#índice)

## Collections

Las collections se diferencian de los arrays ya que si se agrega un dato se crea una nueva posición, si se elimina un dato su posición deja de existir.

Collections es más similar a una lista en Python.

Creamos una collection con `Set`

![add](https://i.ibb.co/bs5QP4c/image.png)

![remove](https://i.ibb.co/cDJ4bbC/image.png)

---

[Índice](#índice)

## Range

Range es un conjunto de celdas de una hoja de Excel.

```VB
'Rango
Range("A1:C5")
'Columna
Range("A:A")
'Fila
Range("3:3")
'No contiguas
Range("A1:B8, D9:G16")
'Cells
Range(Cells(1, 1), Cells(10, 8))
```

[Índice](#índice)

### Propiedades

- **Value2/Value**: El primero es más rápido
- **Text**
- **Count**: Celdas en el rango
- **Interior.Color**: Celdas en el rango
- **Column**
- **Row**
- **Rows.Count**: El número de filas que hacen parte del rango
- **Columns.Count**: El número de columnas que hacen parte del rango
- **Address**: Devuelve la dirección de la celda. `"$A$1:$B$3"`
- **HasFormula**: Boolean, dice si todo el rango posee fórmulas
- **Font**
  - **Name**
  - **Size**
  - **Color**
- **Formula**: Devuleve un array con las formulas que contiene cada celda el rango
- **NumberFormat**: Si todas las celdas del rango poseen el mismo tipo de formato, devuelve el formato.
- **End(<dirección>)**
  - **xlUp**
  - **xlToRight**
  - **xlToLeft**
  - **xlDown**

[Índice](#índice)

### Métodos

- **Select**
- **Copy**
- **Paste**
- **Clear**
- **Delete**
- **Set**

---

[Índice](#índice)

## Condicionales

[Índice](#índice)

### If

```VB
If <condicion1> Then
    <...>
ElseIf <condicion2> Then
    <...>
Else
    <...>
End If
```

[Índice](#índice)

### Select Case

```VB

'Define un parámetro como entrada
Dim semestre As Integer
semestre=Cells(3,2)

'Inicio de la estructura
Select Case semestre

    'Primer caso contemplado
    Case 1
        MsgBox"Primiparo"

    Case 2 To 7
        MsgBox"Regular"

    Case 8,9,10
        MsgBox"Fin de carrera"

    'Característica para resto de casos
    Case Else
        MsgBox"Graduado"

'Cierre de estructura
End Select
```

---

[Índice](#índice)

## Estructuras Determinadas

Se especifica el número de datos a recorrer

[Índice](#índice)

### For

```VB
tamano = Range("B2", Range("B2").End(xlDown)).Rows.Count
For i = 1 To tamano Step 3
    a = a + 2

    If <...> Then
        Continue For
    End If
    If <...> Then
        Exit For
    End If

Next i
```

[Índice](#índice)

### For Each

Para recorrer objetos como: Range, Arrays, Collections.

```VB
Function SumaImpar(y As Range) As Integer

For Each celda In y

    If celda Mod 2 <> 0 Then
        SumaImpar = SumaImpar + celda
    End If

Next celda
```

---

[Índice](#índice)

## Estructuras Indeterminadas

Si no se le estabalece una condición se forma un bucle infinito
[Índice](#índice)

### Do While

No termina hasta que la condición se cumpla

```VB
contador = 0
Do While contador < 30
    <...>
    contador = contador + 1

    If <...> Then
        Continue Do
    End If
    If <...> Then
        Exit Do
    End If
Loop

```

[Índice](#índice)

### Do Until

No termina hasta que la condición se cumpla

```VB
contador = 0
Do Until contador = 30
    <...>
    contador = contador + 1
Loop

```

[Índice](#índice)

### While

No termina hasta que la condición deje de cumplirse

**Considerado obsoleto**

```VB
contador = 0
While <condicion>
    <...>
    contador = contador + 1
Wend
```

---

[Índice](#índice)

## Function

Si creas una función en VBA puedes usarla también en Excel.

La función retorna el valor que se le dé a la _'variable'_

```VB
Function ejemploFuncion(x As Integer, Optional y As Boolean) As Double
    <...>
    ejemploFuncion = 3
End Function
```

- `ByVal`
- `ByRef`
- `ParamArray`

---

[Índice](#índice)

## Eventos

- Relacionados al Libro

En el objeto ThisWorkbook seleccionamos WorkBook y seleccionamos uno en la lista con todos los posibles eventos.

- Relacionados a una Hoja
  En el objeto Hoja1 seleccionamos WorkSheet y seleccionamos uno en la lista con todos los posibles eventos.

---

[Índice](#índice)
