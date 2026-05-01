# Laboratorio 5: Adquisición de señales ECG con BITalino

  

## 1.  Introducción
El laboratorio realizado hizo uso del kit BITalino (r)evolution Board y el software OpenSignals (r)evolution. Estas herramientas permiten la adquisición y visualización de señales fisiológicas respectivamente. En el contexto del laboratorio, se utilizaron para obtener y analizar los ECG, todo mediante el uso de electrodos colocados en configuración para cada derivación medida: I, II y III.

## 2.  Metodología
**Kit BITalino (r)evolution:**
El kit es una plataforma todo-en-uno que contiene diferentes sensores y electrodos necesarios para adquirir una gran variedad de señales fisiológicas. Este kit contiene los siguientes componentes:
-   Placa BITalino (r)evolution
-   Electrodos
-   Cable de 3 vías (para EMG/ECG/EEG) de 30 cm.
-   Cable de 2 vías (para EDA) de 10 cm.
-   Batería Li-Po 3.7 V, 500 mAh

<div align="center">
<img width="400" height="400" alt="bitalino_kit" src="https://github.com/user-attachments/assets/93c523c5-eeea-46d9-bde6-6dd9f19d75ca" />
</div>
<div align="center">  
Figura 1. Kit BITalino
</div><br>

**Laptop como módulo de procesamiento de datos:**
Laptop con Windows 11 y el software OpenSignals (r)evolution instalado para la adquisición, visualización y almacenamiento de las señales.

<div align="center">
<img width="650" height="150" alt="opensignals_logo_small-1024x241" src="https://github.com/user-attachments/assets/606cad60-55d1-401c-9253-378ab69e5927" />
</div>
<div align="center">  
Figura 2. Software OpenSignals
</div><br>

### 2.3. Sujetos de estudio
Participó voluntariamente un estudiante del curso “Introducción a Señales Biomédicas” de la Universidad Peruana Cayetano Heredia, sin antecedentes de enfermedades cardíacas ni otras afecciones clínicas.

### 2.4. Derivaciones del electrocardiograma (ECG)
Se trabajó con las derivaciones bipolares de Einthoven (1):
-   Derivación I: brazo derecho (RA) a brazo izquierdo (LA)
-   Derivación II: brazo derecho (RA) a pierna izquierda (LL)
-   Derivación III: brazo izquierdo (LA) a pierna izquierda (LL)

<div align="center">
<img width="606" height="291" alt="derivadas" src="https://github.com/user-attachments/assets/671ea6c5-ffbb-407d-b84b-2d3ebf01f4b3" />
</div>
<div align="center">  
Figura 3. Posición de electrodos para obtener las derivadas del ECG.
</div><br>


Siguiendo la guía del BITalino, los electrodos se colocaron en regiones equivalentes sobre el cuerpo, específicamente en ambos pectorales, aproximando RA y LA y la cresta iliaca izquierda (LL), en este último priorizamos la zona ósea para obtener un mejor resultado.

<div align="center">  
<img width="506" height="506" alt="derivaciones2" src="https://github.com/user-attachments/assets/1a40f22f-a140-41e8-807e-6b10a818b36a" />
</div>
<div align="center">  
Figura 4. Ejemplo de señales de las derivaciones I, II y III (1).
</div><br>


### 2.5. Actividades a realizar

**Colocación de electrodos**
-   Para la adquisición de la señal de electrocardiografía (ECG) se utilizaron tres electrodos desechables conectados al sensor de ECG ensamblado de BITalino.
-   Los electrodos se dividen en: Positivo, Negativo y Referencia.
-   Siguiendo el sistema de derivaciones bipolares de Einthoven descrito en el manual HomeGuide #2 de PLUX , estos se colocaron inicialmente en ambos pectorales y la cresta ilíaca izquierda. Para obtener las derivaciones I, II y III, se intercambiaron las conexiones de los electrodos según el sistema de Einthoven, tal como indica la guía se cambiaron la posición de los electrodos en las 3 derivaciones necesarias para cada toma de muestras.

<div align="center">  
<img width="267" height="318" alt="derivaciones3" src="https://github.com/user-attachments/assets/02a71ef7-3559-4524-97df-3a353f78829f" />
</div>
<div align="center">  
Figura 5. Imagen referencial de colocación de electrodos y sus derivadas (2).
</div><br>

**Adquisición de señales**

Para cada derivación (I, II y III), se realizaron las siguientes mediciones: <br>

**1.  ECG basal**

Registro en reposo durante condiciones normales de respiración, minimizando el movimiento.

**2.  Hiperventilación**

El sujeto realizó inspiraciones largas y exhalaciones cortas, registrándose la señal ECG después de este proceso.

**3.  Ejercicio físico**

El sujeto realizó aproximadamente 2 minutos de burpees para inducir un aumento de la frecuencia cardíaca.
Inmediatamente después del ejercicio, se registró la señal ECG.

**4.  Hipoventilación**

El sujeto contuvo la respiración el máximo tiempo posible luego de hacer ejercicio.

----------

 
**Archivo de datos de las señales adquiridas**
-   Documentos (Laboratorios/documentos/documentos_lab5.rar)
-   Programa de ploteo (Jupyter Notebook) (Laboratorios/documentos/ploteo_laboratorio_5.ipynb)

  
## 3. Resultados
A continuación se muestran los resultados obtenidos ploteados en OpenSignals y Python respectivamente. En este último se trató la señal y se multiplicó por -1 debido a que se obtuvieron señales con picos negativos, esto se hizo para obtener una señal más clara y apreciar su morfología.

  

### 3.1 Basal:

<div align="center">
  
| I Derivación |
|----------|
| <img width="602" height="117" alt="basal_1a" src="https://github.com/user-attachments/assets/6fc15355-c3b4-42d8-9dce-2a3e16aab953" /> |
| <img width="602" height="176" alt="basal_1b" src="https://github.com/user-attachments/assets/6a98e8c7-193f-45f0-80be-76f815f3f653" /> |

</div>
<div align="center">  
Figura 6. Medición basal primera derivación (DI) en OpenSignals y Python.
</div><br>


<div align="center">
  
| II Derivación |
|----------|
| <img width="602" height="124" alt="basal_2a" src="https://github.com/user-attachments/assets/431eadae-ed18-44ae-a122-19fccefde57e" /> |
| <img width="602" height="176" alt="basal_2b" src="https://github.com/user-attachments/assets/3c13c52d-d763-421a-84af-e91762dcd32a" /> |
</div>

<div align="center">  
Figura 7. Medición basal segunda derivación (DII) en OpenSignals y Python.
</div><br>


<div align="center">
  
| III Derivación |
|----------|
| <img width="602" height="116" alt="basal_3a" src="https://github.com/user-attachments/assets/93e21b91-9620-4e1c-bfdd-bdec617f038f" /> |
| <img width="602" height="176" alt="basal_3b" src="https://github.com/user-attachments/assets/40287f8d-3575-45af-a1bf-04bc6899629b" /> |

</div>
<div align="center">  
Figura 8. Medición basal tercera derivación (DIII) en OpenSignals y Python.
</div><br>

### 3.2 Burpees:

<div align="center">
  
| I Derivación |
|----------|
| <img width="602" height="117" alt="burpees_1a" src="https://github.com/user-attachments/assets/75195743-0c47-4ea8-82de-b4d67796a706" /> |
| <img width="602" height="176" alt="burpees_1b" src="https://github.com/user-attachments/assets/1358cb1d-1544-46de-879d-ef9272827a3c" /> |

</div>
<div align="center">  
Figura 9. Medición después de burpees primera derivación (DI) en OpenSignals y Python.
</div><br>

<div align="center">
  
| II Derivación |
|----------|
| <img width="602" height="121" alt="burpees_2a" src="https://github.com/user-attachments/assets/f480bd47-0709-4f9c-b741-9017d79aeea7" /> |
| <img width="602" height="175" alt="burpees_2b" src="https://github.com/user-attachments/assets/607adebe-e51b-4cda-a8ff-41dc3f2a14c6" /> |

</div>
<div align="center">  
Figura 10. Medición después de burpees segunda derivación (DII) en OpenSignals y Python.
</div><br>


<div align="center">
  
| III Derivación |
|----------|
| <img width="602" height="119" alt="burpees_3a" src="https://github.com/user-attachments/assets/faa8ca05-0bca-4bb3-a795-997d82213ab6" /> |
| <img width="602" height="176" alt="burpees_3b" src="https://github.com/user-attachments/assets/76d09423-6788-4cd9-85e1-2cb1e10ef434" /> |

</div>
<div align="center">  
Figura 11. Medición después de burpees tercera derivación (DIII) en OpenSignals y Python.
</div><br>

### 3.3 Hiperventilación

<div align="center">
  
| I Derivación |
|----------|
| <img width="602" height="123" alt="hiper_1a" src="https://github.com/user-attachments/assets/d53b11fb-7e8b-460b-9939-ff7a9a865f12" /> |
| <img width="602" height="176" alt="hiper_1b" src="https://github.com/user-attachments/assets/3bfefe29-8ce1-42c6-b9c4-4156c6bab81a" /> |

</div>
<div align="center">  
Figura 12. Medición en hiperventilación primera derivación (DI) en OpenSignals y Python.
</div><br>

<div align="center">
  
| II Derivación |
|----------|
| <img width="602" height="123" alt="hiper_2a" src="https://github.com/user-attachments/assets/dbb055f4-0ce5-45c0-9cb5-bc49915d9320" /> |
| <img width="602" height="176" alt="hiper_2b" src="https://github.com/user-attachments/assets/c185cc4e-a760-4ee5-bd98-5133313e1f3d" /> |

</div>
<div align="center">  
Figura 13. Medición en hiperventilación segunda derivación (DII) en OpenSignals y Python.
</div><br>

<div align="center">
  
| III Derivación |
|----------|
| <img width="602" height="119" alt="hiper_3a" src="https://github.com/user-attachments/assets/43744cdc-bdb3-4ebe-abdf-3cb1132bda94" /> |
| <img width="602" height="176" alt="hiper_3b" src="https://github.com/user-attachments/assets/12066ef7-5696-4010-ba5b-d8a2026cf9f9" /> |

</div>
<div align="center">  
Figura 14. Medición en hiperventilación tercera derivación (DIII) en OpenSignals y Python.
</div><br>

### 3.4 Hipoventilación

<div align="center">
  
| I Derivación |
|----------|
| <img width="602" height="119" alt="hipo_1a" src="https://github.com/user-attachments/assets/f8b9ff06-fce7-4087-8dfa-7cb2df78ced8" /> |
| <img width="602" height="176" alt="hipo_1b" src="https://github.com/user-attachments/assets/398d320f-1639-44f6-8c52-87056ed5460b" /> |

</div>
<div align="center">  
Figura 15. Medición en hipoventilación primera derivación (DI) en OpenSignals y Python.
</div><br>

<div align="center">
  
| II Derivación |
|----------|
| <img width="602" height="119" alt="hipo_2a" src="https://github.com/user-attachments/assets/d4f08f29-f522-4356-bea2-7fd40c56c221" /> |
| <img width="602" height="175" alt="hipo_2b" src="https://github.com/user-attachments/assets/db970572-5153-46ae-9df5-f1f541bf9645" /> |

</div>
<div align="center">  
Figura 16. Medición en hipoventilación segunda derivación (DII) en OpenSignals y Python.
</div><br>

<div align="center">
  
| III Derivación |
|----------|
| <img width="602" height="119" alt="hipo_3a" src="https://github.com/user-attachments/assets/0b706eba-f71d-4a11-b25d-80ef86266025" /> |
| <img width="602" height="176" alt="hipo_3b" src="https://github.com/user-attachments/assets/1c5eefb4-f3d0-48f6-baa1-df99f6ea154f" /> |

</div>
<div align="center">  
Figura 17. Medición en hipoventilación tercera derivación (DIII) en OpenSignals y Python.
</div><br>

### 3.5 Transformada de Fourier

<div align="center">  
<img width="602" height="223" alt="fourier1" src="https://github.com/user-attachments/assets/70e6a465-1e00-417c-8e13-8b77a0434c53" />
</div>
<div align="center">  
Figura 18. Fourier del ECG.
</div><br>

<div align="center">  
<img width="602" height="223" alt="fourier2" src="https://github.com/user-attachments/assets/2aa891a4-1dc6-4895-b7fa-8cda09ca53bd" />
</div>
<div align="center">  
Figura 19. FFT del ECG.
</div><br>

<div align="center">  
<img width="602" height="227" alt="fourier3" src="https://github.com/user-attachments/assets/ebcae22f-21f7-440a-a676-a5a8c77ff947" />
</div>
<div align="center">  
Figura 20. FFT del ECG en dB.
</div><br>


## 4. Discusión
Los resultados obtenidos muestran el análisis de las 3 derivaciones (DI, DII, DII) del sujeto de estudio bajo diferentes condiciones fisiológicas: Basal, ejercicio (burpees), hiperventilación e hipoventilación; medidos con un BITalino. Estas derivaciones permiten observar la actividad eléctrica del corazón desde distintos ángulos del cuerpo, proporcionando una representación vectorial de la despolarización cardíaca, así como analizar cómo la actividad cardíaca responde a cambios en la demanda metabólica y en la regulación autonómica.

Cabe señalar que para todas las derivaciones obtenidas, las señales presentaron un complejo QRS invertido, por lo que se multiplicaron cada una por un factor de -1 para obtener la morfología esperada.

### 4.1. Condiciones basales
En primer lugar, se midieron las tres derivaciones para un estado en reposo (basal). La toma de señales en este estado permite obtener un ecocardiograma (ECG) con ritmo regular, frecuencia cardiaca estable y complejos QRS.

<div align="center">  
<img width="471" height="423" alt="ecg_basal" src="https://github.com/user-attachments/assets/cab30260-a41e-4da0-88c9-891dd66d9a62" />
</div>
<div align="center">  
Figura 21. ECG basal.
</div><br>

Aún así, se obtuvieron ciertos cambios en la forma que suele distinguir al complejo QRS. En condiciones fisiológicas típicas, la onda S suele presentar una mayor deflexión negativa en comparación con la onda Q. Sin embargo, en los resultados obtenidos se observó el comportamiento opuesto, donde la onda Q presentó mayor amplitud negativa que la onda S (3). Este hallazgo no necesariamente indica la presencia de una alteración patológica, sino que puede atribuirse a factores técnicos asociados al proceso de medición, como la presencia de ruidos en la señal y la inversión de estas, que requirió multiplicar cada una por un factor negativo.

Para la derivación I (DI), la actividad eléctrica se observa desde el brazo derecho hacia el brazo izquierdo, en un eje horizontal. Esta derivación permite evaluar principalmente la propagación lateral del impulso eléctrico a través de los ventrículos (1). Aquí, el complejo QRS suele ser positivo, así como se observa en la imagen anterior. Esto sucede porque el vector de despolarización se dirige hacia el lado izquierdo del cuerpo, apuntando hacia donde se está observando el corazón.

La derivación II (DII) mide la diferencia de potencial entre el brazo derecho y la pierna izquierda, alineándose con la dirección predominante del vector eléctrico cardíaco (1). Suele presentar un complejo QRS de mayor amplitud debido a que su eje se alinea estrechamente con la dirección predominante de la despolarización ventricular. En las gráficas obtenidas se observa que la derivación III presenta mayores amplitudes, posible causa de contacto desigual de electrodos o ruidos.

Por su parte, la derivación III (DIII) registra la diferencia de potencial entre el brazo izquierdo y la pierna izquierda, ofreciendo una perspectiva oblicua diferente dentro del plano frontal (1). En esta derivación, se puede obtener complejos QRS tanto positivos como negativos.

### 4.2. Condiciones después de ejercicio (Burpees)

El sujeto de estudio realizó 2 minutos de burpees (sentadilla, plancha y salto vertical) con el fin de aumentar la demanda metabólica. Dicho ejercicio conlleva a cambios en la amplitud y morfología del electrocardiograma.

<div align="center">  
<img width="919" height="410" alt="comp1" src="https://github.com/user-attachments/assets/ca7afc4a-ed1c-46e3-87d4-73fcaa516f4e" />
</div>

<div align="center">  
Figura 22. ECG basal y burpees.
</div><br>

Se puede observar en las dos gráficas presentadas las diferencias entre el ECG en estado basal y después de realizar burpees. Se aprecia un incremento notable en la frecuencia cardiaca (mayor cantidad de complejos QRS durante un mismo periodo de tiempo), lo cual se refleja en la disminución de los intervalos RR y un aumento en la amplitud.

Asimismo, las tres derivaciones presentan un aumento en el nivel de ruido, atribuible tanto al movimiento corporal durante el ejercicio como a la actividad muscular, lo que introduce artefactos en la señal. Se puede apreciar que las ondas P y T son menos visibles y difíciles de identificar, así como la presencia de un desplazamiento (offset) de la línea base respecto a cero en todas las señales. Dicho offset puede presentarse por la agitación del individuo después de una actividad física, que conlleva a movimientos del tórax por respiración agitada y cambios en la impedancia de la piel por sudoración (4).

En cuanto a la morfología, la derivación II tiende a conservar una mejor definición de las ondas, especialmente del complejo QRS, debido a su alineación con el eje eléctrico principal del corazón, lo cual puede verificarse en su respectiva gráfica (1).

En conjunto, los cambios observados en las tres derivaciones durante el ejercicio son coherentes con la respuesta fisiológica esperada, caracterizada por un aumento de la frecuencia cardíaca, mayor actividad eléctrica y presencia de artefactos.

### 4.3. Condiciones después de hiperventilación

Tras la fase de hiperventilación, se observan ciertos cambios en las tres derivaciones asociados principalmente a alteraciones en la regulación autonómica y concentración de dióxido de carbono en sangre (5).


<div align="center">  
<img width="917" height="414" alt="comp2" src="https://github.com/user-attachments/assets/3a1c35fa-a5d7-4dc8-80e9-bd9a0f5ba5e3" />
</div>

<div align="center">  
Figura 23. ECG basal e Hiperventilación.
</div><br>

En las gráficas presentadas se aprecia una ligera variabilidad en la frecuencia cardiaca, evidenciada por pequeñas fluctuaciones en los intervalos RR. Esta respuesta puede atribuirse a cambios en el balance simpático-parasimpático inducidos por la hipocapnia, más que a un aumento de la demanda metabólica. Asimismo, se observa un desplazamiento de la línea base (offset), el cual puede relacionarse con el patrón respiratorio acelerado, generando movimientos torácicos que afectan la estabilidad de la señal (5).

En cuanto a la morfología, se ha perdido cierta definición de las ondas características, especialmente las P y T. Al igual que con los burpees, el movimiento del tórax puede provocar artefactos durante la respiración forzada.

Ante ello, en la segunda derivación (DII), a diferencia de las otras dos derivaciones (DI y DIII), se observan estos cambios de forma más pronunciada debido a su alineación con el eje eléctrico principal del corazón. Por su parte, las derivaciones I y III presentan una mayor variabilidad en la amplitud, lo cual se refleja en una menor estabilidad de la señal.

En conjunto, estas diferencias reflejan cómo la hiperventilación no altera directamente la generación de la señal eléctrica cardíaca, sino su proyección sobre cada derivación y calidad de la medición.

### 4.4. Condiciones después de hipoventilación
Para la hipoventilación voluntaria se exigió al sujeto de estudio aguantar la respiración hasta donde pueda. Esto crea un estado donde el cuerpo no recibe suficiente oxígeno para satisfacer sus necesidades, aumenta el CO2 (hipercapnia) y disminuye el O2. En el electrocardiograma se aprecia en general, una tendencia a aumentar la frecuencia cardiaca (6).

<div align="center">  
<img width="917" height="414" alt="comp3" src="https://github.com/user-attachments/assets/59a83983-a135-4c7a-9e45-46c9d73d6a5a" />
</div>

<div align="center">  
Figura 24. ECG basal e Hipoventilación.
</div><br>

En las gráficas presentadas se aprecia que los complejos QRS tienen picos más altos, así como más densidad en el mismo intervalo de tiempo que el ECG basal. Este aumento de la frecuencia cardiaca se produce como mecanismo compensatorio ante el aumento de CO2.

A diferencia de condiciones dinámicas como el ejercicio o la hiperventilación, la señal presenta una mayor estabilidad general, lo que permite una mejor definición del complejo QRS y mejor claridad de las ondas P y T respecto a las actividades anteriores. En cuanto a la línea base, puede observar que en las tres derivaciones, esta es muy leve a comparación de actividades que conllevan a una respiración forzada y pueda comprometer la medida de la señal debido a movimientos del tórax (6).

Al igual que en las anteriores mediciones, la derivación II (DII) presenta una mayor amplitud y formas más definidas debido a la alineación que tiene esta con el vector eléctrico cardiaco.

En conjunto, la hipoventilación voluntaria por aguantar la respiración conlleva a un ligero aumento de la frecuencia cardiaca, pero sin una agitación excesiva del individuo. En consecuencia, se obtienen señales más estables y con mejor morfología que las que requieren un aumento de la actividad metabólica, como los burpees o hiperventilación.


### 4.5. Limitaciones

 
-   **Ruido de línea e interferencia electromagnética**
A pesar de haberse realizado la adquisición en un ambiente de laboratorio sin fuentes de interferencia evidentes (celulares apagados, laptops alejadas), la señal ECG es intrínsecamente susceptible al ruido de la red eléctrica (60Hz en caso de Perú). La literatura establece que esta es una de las fuentes de ruido más significativas en sistemas de medición ECG, especialmente cuando se usan electrodos convencionales Ag/AgCl en entornos no clínicos. Esta interferencia puede enmascarar componentes de baja amplitud de la señal, como la onda P o el segmento ST, comprometiendo el análisis morfológico (7).

 

-   **Artefactos por movimiento**
Durante el protocolo de adquisición se realizaron ejercicios de respiración profunda, hiperventilación voluntaria y actividad física (burpees). El movimiento de los cables y electrodos respecto a la piel genera artefactos de baja frecuencia que pueden distorsionar la señal ECG. En el estudio “Motions artifacts in capacitive ECG monitoring systems: a review of existing models and reduction techniques", se destaca que los artefactos por movimiento son una de las principales limitaciones en sistemas ECG ambulatorios, ya que la variación de la impedancia electrodo-piel durante el movimiento puede simular arritmias o alteraciones del segmento ST (7). En nuestro estudio, si bien se intentó minimizar el movimiento durante los registros basales, los ejercicios respiratorios y las transiciones entre posiciones introdujeron artefactos visibles en la señal.

  
-   **Variabilidad anatómica para colocación de electrodos**
La colocación manual de los electrodos introduce variabilidad en la señal adquirida. Diferencias de pocos centímetros en la ubicación de los electrodos, así como características anatómicas individuales (como el grosor del tejido adiposo o la composición corporal), afectan la amplitud y morfología del ECG. En un estudio reciente sobre dispositivos mini ECG se reportó que pacientes con índice de masa corporal (IMC) elevado, presentaron menores desviaciones del segmento ST en comparación con el ECG de 12 derivaciones, atribuyéndose el efecto al tejido adiposo de la pared torácica (8). En el estudio no se registró el IMC del participante, y al ser solo uno, tampoco hubiera sido posible realizar una comparativa.

  

-   **Limitaciones del sistema BITalino**
El Kit BITalino utilizado en el laboratorio, emplea un ADC de 10 bits y permite registrar únicamente una derivación a la vez. A diferencia del ECG clínico estándar de 12 derivaciones, esta configuración de una sola derivación (lead I, II o III) no permite una evaluación completa del eje cardíaco ni la localización topográfica de posibles anomalías. La baja resolución del ADC (10 bits vs. los 16-24 bits de sistemas clínicos) también puede limitar la capacidad de detectar ondas de baja amplitud, como la onda P (9).

  

-   **Normalización y ausencia de referencia gold standard** 
    Este estudio no contó con un gold standard de referencia, como lo sería usar un ECG con 12 derivaciones simultáneas, para validar la morfología de las ondas detectadas (P, QRS, T). Tampoco se realizó una calibración en milivoltios que permita convertir las unidades digitales del ADC a µV reales, esto limita la comparación de amplitudes con valores clínicos de referencia. Todo esto impide cuantificar la exactitud diagnóstica del sistema BITalino en términos de sensibilidad y especificidad para la detección de anomalías.  
      
    

-   **Tamaño de muestra reducido**
El estudio incluyó únicamente a un participante voluntario, estudiante del curso sin patologías cardíacas conocidas. Este tamaño de muestra no permite generalizar los hallazgos a poblaciones más diversas (diferentes edades, condiciones patológicas, o características antropométricas). Además, no se evaluó la reproducibilidad de las mediciones mediante análisis test-retest con varios días de diferencia.


## 5. Referencias

1.  Meek S, Morris F. Introduction. I—Leads, rate, rhythm, and cardiac axis. BMJ. 2002 Feb 16;324(7334):415–8. doi: 10.1136/bmj.324.7334.415. PMID: 11850377; PMCID: PMC1122339.
    
2.  PLUX Biosignals, HomeGuide #2: Electrocardiography (ECG), Lisboa, Portugal, 2021.
    
3.  Azcona L. El electrocardiograma. En: López Farré A, Macaya Miguel C, editores. Libro de la salud cardiovascular del Hospital Clínico San Carlos y la Fundación BBVA. Bilbao: Fundación BBVA; 2009. p. 49–56.
    
4.  Kocsis L, Pap Z, László SA, Gábor-Kelemen H, Szabó IA, Heidenhoffer E, et al. Exercise-Induced Electrocardiographic Changes in Healthy Young Males with Early Repolarization Pattern. Diagnostics. 2024;14(10):980. doi: 10.3390/diagnostics14100980.
    
5.  Hawkins SM, Guensch DP, Friedrich MG, Vinco G, Nadeshalingham G, White M, et al. Hyperventilation-induced heart rate response as a potential marker for cardiovascular disease. Scientific Reports. 2019;9:17887. doi:10.1038/s41598-019-54375-9.
    
6.  O’Croinin D, Ní Ghriallais F, Scully M, et al. Influence of hypercapnia and hypercapnic hypoxia on the heart rate response to apnea. Experimental Physiology. 2024. doi:10.1113/EP091234.
    
7.  M. Khalili, H. GholamHosseini, A. Lowe, and M. M. Y. Kuo, "Motion artifacts in capacitive ECG monitoring systems: a review of existing models and reduction techniques," Med. Biol. Eng. Comput., vol. 62, pp. 3599–3622, Jul. 2024.
    
8.  A. Zepeda-Echavarria, R. R. van de Leur, and P. A. Doevendans, "On the detection of acute coronary occlusion with the miniECG," Eur. Heart J. Digit. Health, vol. 5, no. 6, pp. 656–657, Sep. 2024.
    
9.  A. Salimi, S. V. Kalmady, A. Hindle, O. Zaiane, and P. Kaul, "Exploring best practices for ECG signal processing in machine learning," arXiv preprint arXiv:2311.04229, 2023.
