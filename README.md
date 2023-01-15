
# Infra

## Context
Infra server for Care microservice. this repo contains how the docker images needed to run the entire application. 
For more information regarding the project and the architecture can it be found at **[Medicine-Tracker](https://github.com/vcaf/Medicine-Tracker)** repository. 

## Running the project 
The images are stored on my private Docker hub, and with no access to the repo each image have to be build first.
1. build each service locally which are the following:
	- [UserMedicineInventory](https://github.com/vcaf/UserMedicineInventory)
	- [MedicineInventory](https://github.com/vcaf/MedicineInventory)
	- [CareFrontend](https://github.com/vcaf/CareFrontend)
2. After the images have been build locally is there changes that need to be made for each placement where an image is named. This is because the naming used are to find the image on my private docker hub which will have to be changed to the images stored on your local docker.
3. After each images has been changed is it time to run the project. 
<b> Note to anyone that can access my private docker hub:</b> if you have access to the private docker hub you can start at step 3.
First locate to the correct folder where the docker compose file is.

4. Next is time to run the docker file with the following: <pre><code>docker compose up -d</code></pre>
6. The project should now be running locally on docker.


## Running the project on Azure
The project is running on Azure Kubernetes service. If changes are made to the AKS folders and would need to be updated on azure, is the following steps handy.

1. open your command prompt.
2. login to azure : <pre><code>az login</code></pre>
3. locate to the folder where changes have been made
4. now apply the new files to azure: <pre><code>kubectl apply -f . </code></pre>
5. the files should now be updated on azure.
