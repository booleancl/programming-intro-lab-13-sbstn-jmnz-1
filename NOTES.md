## Repaso SQL

SQL es un lenguaje de programación para bases de datos. Su traducción literal sería Lenguaje Estructurado De Consultas (Structured Query Language)

SQL es un lenguaje insensible a mayúsculas y minúsculas. "select" == SELECT.

En sql las tablas tienen columnas que tendrán información de cierto **tipo**

>Como buena práctica los nombres de las tablas deben ser en **plural**.

Llave primaria: con valor único y no nulo.

CSV: Es un formato de archivo muy popular en los negocios. A partir de XLS se pueden exportar datos en CSV y también importar. 'Valores separados por coma'.

```sql
SELECT <column>
FROM <table>;
```

La sentencia **WHERE** es para filtar información

```sql
SELECT <column>
FROM <table>;
WHERE <column> <condition>;
```

Ejemplo de varias condiciones usando **AND**
```sql
SELECT name, country, area
FROM cities
WHERE area < 1100
AND country = 'Japan';
```

### Ejemplo usando **OR**

```sql
SELECT name, country, area
FROM cities
WHERE area < 1100
OR country = 'Japan';
```

### Ejemplo ordenando los resultados en forma ascendente

ASC es la forma por defecto del ORDER BY

```sql
SELECT name, country, area
FROM cities
ORDER BY area;
```

## Ejemplo con WHERE, OR y ORDER

```sql
SELECT name, country, area
FROM cities
WHERE area < 1100
OR country = 'Japan'
ORDER BY area;
```

## Ejemplo descendente

```sql
SELECT name, country, area
FROM cities
WHERE area < 1100
OR country != 'Japan'
ORDER BY area DESC;
```

>Nota: Distinto puede ser <> o !=

## Campos o columna calculados con AS (como)

```sql
SELECT name, population/area AS density 
FROM cities
ORDER BY density DESC;
```

## Contando elementos con COUNT

```sql
SELECT COUNT(name)
FROM cities
WHERE country = 'India';
```

## Limitar los resultados con **Limit**

```sql
SELECT name, population/area AS density 
FROM cities
ORDER BY density DESC
LIMIT 2;
```

