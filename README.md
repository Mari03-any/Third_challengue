# Third_challengue
## pdc_unal_Maria_Fernanda_Parra_Osorio
Este reto consiste en determinar en una serie de pasos hasta un número n.
<tr style="text-align: left; vertical-align: middle;" bgcolor="#">
		<th>
			<p align="left"><b>Inicio</b><br>
			PASO 1. Crear una lista de números naturales desde 2 hasta n <br>
			PASO 2. Dividir n sobre 2 <br>
			PASO 3. Crear una nueva lista con los valores numericos <br>
				PASO 2.2. Si el residuo de la división es cero, n no es número primo <br>
				PASO 2.3. Sino, n es número primo <br>
                                PASO 2.4. El número 2 es una excepción <br>
			<b>Fin</b><br></p>
		</th>
	</tr>
 
### Pseudocode
```pseudocode
[variables]
n : entero
inicio
  n := 2
  Mientras (n>2) hacer
    Si modulo(2,n) == 0 entonces
      escribir("n no es número primo")
    sino
      escribir("n es número primo")
    n := n + 1
  Fin mientras
fin
```

### Diagrama de flujo
```mermaid
flowchart TD
    A[Inicio] --> B(numero n) --> c(Lista desde 2 hasta n) --> D(n=2)
    D--> E{Residuo de la division entre es cero?}
    E -->|si| F[i no es primo]
    E -->|no| G[i es primo]
    H[n:n+1] --> I{n≤2?}
    F --> H
    G --> H
    I -- si--> J[No pueden ser irracionales]
    I --> K[El 2 es número primo]
    J --> E
    K --> L
    I --> |no| L(Fin)
