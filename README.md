------------------------------------------------------------------------

------------------------------------------------------------------------

# MODELO DE EVALUACIÓN DE STOCK DE ERIZO

Este repositorio contiene los análisis realizados para la evaluación de stock de Erizo  para las tres unidades de stock (Zona X Norte, Zona X Sur y Zona XI) 

**Descripción del contenido de la carpeta "codigos\_admb"**

El código base corresponde a un Modelo de Captura a la talla ("Modbento") creado por cristian.canales\@ifop.cl. Los códigos utilizados para este estudio corresponde a una modificación del "Modbento". Esta modificación es realizada por mariajose.zuniga\@ifop.cl y mauricio.mardones\@ifop.cl se detallará a continuación.

Contiene los códigos de ADMB principalmente MAET.tpl y MAET.dat del modelo de evaluación de stock de erizo de la zona X Norte (MAETXN) , X Sur (MAETXS) y XI (MAETXI).

Los modelos corresponden a modelos anuales (año calendario) con dinámica a la edad e información en tallas (utiliza matriz de probabilidad edad\_talla).

Los principales datos que ingresan al modelo corresponden a los desembarques, CPUE y frecuencia de tallas de la flota. Utiliza un vector de pesos medios a la talla, madurez a la talla, y parámetros de crecimiento y mortalidad natural.

## 

**CARPETAS:**

1.  **codigos\_admb**

-   código fuente (.tpl)
-   datos y controles (.dat)

- **MODELO BASE**
  * MAETXN
  * MAETXS
  * MAETXI
  
- **MODELO ALTERNATIVO**
  * MAETXNa
  * MAETXSa
  * MAETXIa
  
2.  **FUNCIONES**

-   **Fn_DiagramaFase.R** = genera figura de diagrama de fase con banda de plenaexplotación
-   **Fn_Frms.R** = corre código de ADMB que estima los puntos biológicos de referencia, principalmente Frms (archivos de guardan en carpeta llamada "PBR_Analisys")
-   **Fn_MortalidadNatural.R** = corre los escenarios de mortalidad natural (guarda archivos .rep, .dat y .std en carpeta llamada "MortalidadNatural_XN","MortalidadNatural_XS","MortalidadNatural_XI", para caso base)
-   **Fn_Rango_Loo.R** = corre los escenarios de Loo (guarda archivos .rep, .dat y .std en carpeta llamada "RangoLoo_XN","RangoLoo_XS","RangoLoo_XI", para caso base) 
-   **Fn\_Retrospectivo.R** = Corre escenarios de retrospectivo (genera la carpeta con archivos .rep, .dat y .std en carpeta llamada "RetrospectivoXN","RetrospectivoXS","RetrospectivoXI", para caso base)
-   **Fn_Verosimilitud.R** = Corre escenarios para perfil de verosimilitud (genera la carpeta con archivos .rep, .dat y .std en carpeta llamada "VerosimilitudXN","VerosimilitudXS","VerosimilitudXI", para caso base)
-   **functions.R** = lisread (función que lee archivo ".dat") y reptoRlist (función que lee archivo ".rep")
-   **removefile.R** = remueve archivos no deseados al correr códigos de ADMB

3.  **FIGURAS**

-  Carpeta **Figuras** = contiene las figuras generadas por archivo "Informe_Estatus_Erizo_65_21.Rmd"
-  Carpeta **Figuras_Diagnostico** = contiene las figuras generadas por archivo "Figuras_y_Tablas_Erizo2022.Rmd" y "Figuras_y_Tablas_Erizo2022_alternativo.Rmd"

**Códigos en Rmarkdown**

-   **"Informe\_Estatus\_Erizo\_word.Rmd"** = corresponde al informe de estatus del las tres unidades de stock del erizo que debe ser entregado entre diciembre y enero. (generado el 2020)

-   **"Figuras_y_Tablas_Erizo2022.Rmd"** = genera figuras y tablas de modelo base

-   **"Figuras_y_Tablas_Erizo2022_alternativo.Rmd"** = genera figuras y tablas de modelo alternativo

**Archivos:**


-   TemplateWord\_Erizo.docx = es utilizado en el código "Informe\_Estatus\_Erizo\_word.Rmd" para darle el formato deseado (tipo de letra, títulos, etc).

-   Readme\_codADMB.pdf = se describen los archivos de datos y controles (.dat), reporte (.rep), el código fuente (.tpl), los parámetros estimados por el modelo (.par) y parámetros y variables estimadas con error (.std).
