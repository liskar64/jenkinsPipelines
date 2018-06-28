pipeline {
	agent any
	tools{        
		maven 'Maven'  
	       } 
	stages{
		stage('inicio'){
			steps{
				echo 'Bienvenido usuario'
				}
		}
		stage('Pruebas'){
			steps{
			sh 'mvn test'				
			}
		}
		stage('build'){
			steps{
			echo 'Construyendo'
			sh 'mvn package'
			}
		}
		stage ('Ejecucion'){
			steps{
			echo 'Ejecutando el paquete'        
        		sh 'mvn exec:java -Dexec.mainClass="com.pipeline.test.App"' 
			}

		}
	}
	post{
		success{
			echo 'Finalizacion correcta'
		}	
	}
}
