# Docker_Kubernetes_project

# Objectifs:

1- Creation d'une simple application nodeJs.
2- Deployer cette derniere dans un conteneur docker 
3- Utiliser Kubernetes comme outils d'orchestration 


// lancement de minikube start pour la vm 
//bash ssh :C:\Users\kheff\OneDrive\Bureau\ProjetPerso\Demo_Kubernetes :
// $ echo $(minikube docker-env)
 :: pour l'afichage des variables d'envirenement
 
// eval $(minikube docker-env)
:: por l'evaluation et l'execusion 

// echo $DOCKER_HOST
:: le docker hote comme c'est une vm et ne pas se tremper 

//docker build . -t app-nodejs-test:v1
:: creatioon  de l'image de l'application 

4- deployement:
    -soit creaton d'un fichier yml et decrire le processus
    - les commandes :
    $ kubectl create deployment fist-deploy --image app-nodejs-test-v1 
    $ kubectl get deployments
    $ kubectl get pods


5- exposer le service pour qu'il spot acceccible de l'exterierur 
    $ kubectl expose deployment  fist-deploy --type NodePort --port=8080
    ** il va le mapper vers un port d
