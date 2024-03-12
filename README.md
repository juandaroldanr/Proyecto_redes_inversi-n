##  Estimación de cambios individuales y estructurales usando modelos de inferencia o influencia social en redes

## Tabla de Contenido

- [Objetivos](#-objetivos)
- [1. Contexto](#1-contexto)
- [2. Datos](#2-datos)
- [3. Metodología](#3-metodología)
- [4. Referecias](#4-referencias)


## Objetivos

El objetivo general del proyecto es analizar las redes sociales de diferentes inversionistas para caracterizar su comportamiento e identificar los atributos significativos a la hora de financiar compañías. Se espera que los estudiantes sean capaces de aplicar los conocimientos vistos en el curso en un contexto real y llevar a cabo análisis e interpretaciones en el contexto del problema dado, utilizando las herramientas adecuadas.  


## 1. Contexto

Normalmente las compañías buscan fuentes de financiación y dedican esfuerzos a mejorar sus posibilidades de recibir inversiones (Liang & Yuan, 2016). Uno de los problemas que surgen en esta búsqueda de fuentes de financiación es que existen asimetrías de información. Esto ocurre porque las compañías que buscan financiación tienen información acerca de su potencial y de sus oportunidades que los inversionistas no tienen (Shane & Cable, 2002). En este contexto el análisis de redes sociales es una herramienta que permite analizar el comportamiento de los inversionistas teniendo en cuenta sus relaciones con otros. Esto permite conocer lo que los inversionistas están buscando y los factores que determinan su comportamiento al momento de financiar empresas (Liang & Yuan, 2016).  

## 2. Datos

Para lograr el objetivo del proyecto ustedes cuentan con datos de Crunchbase que contienen la información de un conjunto de organizaciones y sus inversionistas. Los datos están organizados en los siguientes archivos de Excel de la siguiente manera: 

• Base inicial: este archivo contiene todos los atributos de los nodos de la red que se va a analizar. Un nodo es una organización y cuenta con los siguientes atributos:   
o Id: Nombre de la empresa.  
o Location: Ubicación de la empresa.  
o Operating Status: Estado de operación de la empresa. Puede estar Activa (active) o Cerrada (closed).  
o Company Type: Indica si la organización es sin ánimo de lucro (non profit) o con ánimo de lucro (profit).   
o Number of Investments: Cantidad total de inversiones realizadas.   
o Number of Lead Investments: Cantidad de inversiones realizadas como inversor principal.  
o Number of Diversity Investments: Cantidad de inversiones diversificadas realizadas. Cuando se realiza una inversión diversificada se destina el dinero a invertir en diferentes portafolios.  
o Number of Exits: Cantidad de veces que en la compañía se han emitido acciones.   
o Number of Lead Investors: Cantidad de inversionistas principales en la compañía.  
o Number of Investors: Cantidad de inversionistas en la compañía.  
o Industry Groups: Grupos de industrias a los cuales pertenecen las organizaciones. La lista de grupos de industrias que podría haber y sus industrias puede encontrarse aquí.  
o Industries: Industrias a las cuales pertenecen las organizaciones. La lista de grupos de industrias que podría haber y sus industrias puede encontrarse aquí.  
o Number of Funding Rounds: Cantidad de rondas de financiación de la empresa.   
o Funding Status: Estado de financiación de la empresa. Puede ser Early Stage Venture, Late State Venture, IPO, M&A, Seed o Private Equity.   
o Last Funding Date: Última fecha de financiación.   
o Last Funding Amount Currency (in USD): Valor de la última financiación en dólares estadounidenses.    
o Last Funding Type: Tipo de la última financiación. Los diferentes tipos de financiación pueden encontrarse aquí.   
o Last Equity Funding Type: Tipo de la última financiación excluyendo la deuda. Los diferentes tipos de financiación pueden encontrarse aquí.  
o Last Equity Funding Amount Currency (in USD): Valor de la última financiación en dólares estadounidenses excluyendo la deuda.  
o Total Funding Amount Currency (in USD): Valor total de dinero recaudado en dólares estadounidenses durante todas las rondas de inversión.   
o Number of Events: Cantidad total de eventos en los que la organización ha aparecido.    
o SEMrush – Monthly Visits: Cantidad de visitas al sitio web de la compañía en el último mes incluyendo visitas al sitio móvil y desktop.    
o SEMrush - Average Visits (6 months): Cantidad promedio de visitas mensuales al sitio web de la compañía en los últimos 6 meses incluyendo visitas al sitio móvil y desktop.    
o SEMrush – Visit Duration: Tiempo promedio que un usuario permanece en la página web de la compañía por visita. Se mide en segundos.   
o Aberdeen - IT Spend Currency (in USD): Monto aproximado en dólares que la compañía invierte anualmente en tecnologías de información (TI).   
o Principales inversionistas: Nombres de los principales inversionistas de la organización.   


Arcos: En el siguiente enlace encuentran el archivo Arcos: https://www.coursera.org/learn/analytics-redes sociales/resources/Rk5wI Este archivo contiene todos los arcos de la red que se va a analizar. Un arco se forma cuando una organización financia a otra. Esta red es dirigida. El archivo contiene la siguiente información:    
o Source: nombre de la compañía inversionista.    
o Target: nombre de la compañía financiada.    


## 3. Metodología

El contenido de las noticias fue procesado mediante algoritmos de PLN para eliminar números, acentos, caracteres especiales, letras mayúsculas, así como palabras referentes a días y meses, dado que las fechas no fueron consideradas. El objetivo era mitigar el impacto que dichos elementos temporales podrían tener en la agregación por temas. Se empleó NLTK para eliminar Stopwords en español y palabras de menos de dos caracteres.

Para extraer las características esenciales de cada noticia, se implementaron en paralelo dos métodos de reducción de palabras a su raíz: Stemming y Lematización. El primero, eliminando prefijos y sufijos tras la tokenización de las noticias usando Snowball Stemmer de NLTK; y el segundo, reduciendo palabras a su lema base con WordNetLemmatizer de NLTK.

## 4. Referencias  
Liang, Y. E., & Yuan, S. T. D. (2016). Predicting investor funding behavior using crunchbase social network features. Internet Research, 26(1), 74–100. https://doi.org/10.1108/INTR-09-2014-0231/FULL/XML  
Shane, S., & Cable, D. (2002). Network Ties, Reputation, and the Financing of New Ventures. Management Science, 48(3), 364–381. http://www.jstor.org/stable/822571  
