pipeline{
    agent none
    options{
        // skipDefaultCheckout()
        
    }
    stages{
        stage("build"){
            // agent any

            // options{
            //     skipDefaultCheckout()
            // }
            
            when { 
                changelog '.* some texts*.' // commit must match this for this stage to execute
                // changeRequest() // only when PR is raised or
                // changeRequest title: "when pr" // must have this pr titles
                // chageset glob: "*.js", caseSensitive: true
                // beforeAgent: true
                
            }

            steps{
                echo "Hello world"
            }
        }
        
        stage("build-with-tags"){
            when {
                buildingTag()
            }

            steps {
                echo "building with tags"
            }
        }
        
//         stage("master"){
//             when {
//                 branch "main"
//             }
            
//             steps{
//                 echo "main deploy"
//             }
//         }

//         stage("dev"){
//             when {
//                 branch "dev" 
//             }
            
//             steps {
//                 echo "dev deploy"
//             }
//         }
        
        stage("indexTrigger"){
            echo "builds on commit"
        }
    }
}
