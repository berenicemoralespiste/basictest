#!groovy

node {

   // ------------------------------------
   // -- ETAPA: Compilar
   // ------------------------------------
   stage 'Compilar'
       // -- Configura variables
       echo 'Configurando variables'
       def mvnHome = tool 'M3'
       // -- Compilando
       echo 'Compilando aplicación'
       sh 'mvn clean compile'



   // ------------------------------------
   // -- ETAPA: Instalar
   // ------------------------------------
   stage 'Instalar'
       echo 'Instala el paquete generado en el repositorio maven'
       sh 'mvn install -Dmaven.test.skip=true'
}