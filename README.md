# Third_challengue
## pdc_unal_Maria_Fernanda_Parra_Osorio
Este reto consiste en determinar en una serie de pasos hasta un número n.
Para esto sabemos que los números primos son divisibles por si mismos y 1.
<tr style="text-align: left; vertical-align: middle;" bgcolor="#">
		<th>
			<p align="left"><b>Inicio</b><br>
			PASO 1. Crear una lista de números naturales hasta n <br>
			PASO 2. Repetir con i <br>
			PASO 3. Dividir i menor que n entre n <br>
				PASO 3.2. Si el residuo de la división es cero, n no es primo <br>
				PASO 3.3. Sino, n es número primo <br>
                                PASO 3.4. El número 2 es una excepción <br>
			<b>Fin</b><br></p>
		</th>
	</tr>
 
### Pseudocode
```pseudocode
[variables]
n : entero
i : entero

inicio
  i := 2
  n := 2
  Mientras (i ≤ n + 1) hacer
    Si modulo(n, i) == 0 entonces
      escribir("n no es número primo")
    sino
      Si (i > n/2) entonces  
        escribir("n es número primo")
           n:= n + 1
           i:= 2
      sino
         i := i + 1
  Fin mientras
fin
```

### Diagrama de flujo
```mermaid
flowchart TD
    A[Inicio] --> B(numero n) --> c(Lista de numeros naturales hasta n) -->D(2 es primo) --> E(n=2) --> F(i=2)
    F--> G{Residuo de la division es cero?}
    G -->|si| H[i no es primo]
    G -->|no| I{i ≥ n/2}
    I -- si --> K[i es primo]
    I -- no --> N
    N[n = n+1]
    N --> G
    N --> O{i ≤ n+1} 
    O -- si --> F
    O -- no --> L(Fin)
