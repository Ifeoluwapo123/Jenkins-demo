pipeline{
    agent none
    // options{
    //             skipDefaultCheckout()
    //         }
    stages{
        stage("build"){
            // agent any

            // options{
            //     skipDefaultCheckout()
            // }
            
            when { // commit must match this for this stage to execute
                changelog '.* some texts*.'
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
    }
}
