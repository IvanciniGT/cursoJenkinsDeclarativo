node {
    stage('Etapa 0'){
        echo 'Dentro de la Etapa 0'
    }
    stage('Etapa 1'){
        try{
            echo 'Dentro de la Etapa 1'
            sh 'exit 1'
            // Esta tarea se ejecura siempre que las anteriores hayan ido bien
            echo 'Despues de la Etapa 1, si va bien'
        }catch (exc){
            // Este sería el caso del catchError
            echo 'Esto solo se va a ejecutar si se ha producido un error'   
            // Este seria el caso failure del Declarativo
            throw exc
        }finally {
            echo 'Esto se ejecuta si hay error o no'   
        }
        echo 'Luego vendrían más tareas después.'
    }
}