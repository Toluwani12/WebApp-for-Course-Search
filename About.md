# Deploy a Full Stack Web Application
> This application provides search functionality and enables the users to search for the courses. These courses are stored and fetched from the PostgreSQL database.

1. Create a cluster. 
`kind create cluster`
![](Images/Pic.png)

2. Containerize and Push the Frontend of the Application
    - Change the directory to /elearning.
    - Create a Docker image.
    ![](Images/Pic1.png)
    - Push this image to Docker Hub.
    ![](Images/Pic2.png)
3. Deploy the Database
    - After I created the deployment file (*database.yaml*), I created it by 
    > `kubectl apply -f database.yaml`. This is in the multiple_Deployments directory.

    I verified the database was created
    ![](Images/Pic3.png)
4. Create a Service for the Database
    - Basically replicated the same in No 3.
    ![](Images/Pic4.png)
5. Deploy the Frontend of the Application
    - I also created the frontend as well using the same method as the backend.This is after creating the yaml files.
    ![](Images/Pic5.png)

    ![](Images/Pic6.png)
6. Create a ConfigMap
7. Access the Application
> `kubectl port-forward svc/app-svc --address 0.0.0.0 31111:3000`

    ![](Images/Pic7.jpg)