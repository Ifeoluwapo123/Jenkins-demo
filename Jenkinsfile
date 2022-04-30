pipeline{
    agent none
    options{
                skipDefaultCheckout()
            }
    stages{
//         stage("build"){
//             agent any

//             // options{
//             //     skipDefaultCheckout()
//             // }

//             steps{
//                 echo "Hello world"
//             }
//         }
        
        stage("build-with-tag"){
            when {
                buildingTag()
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
