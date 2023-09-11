# Provisionando-ambiente-com-Kubernetes

O desafio consiste em configurar um ambiente de desenvolvimento para uma aplicação web baseada em Java e MySQL, usando o Minikube e o Kubernetes.

- Cluster Kubernetes rodando:

  ![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/ba791021-1908-486f-9f30-e2cea9c0c8b1)

       Crie um deployment do MySQL no cluster Kubernetes. 
- Deployment do MySQL:

![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/02d0b042-9db4-4e10-9147-68ae30c0c851)

Evidencia de funcionamento:

![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/27662ebb-f9c2-46e1-86ff-5d39ce241502)

      Crie um serviço para o deployment do MySQL, para que a aplicação possa se conectar a ele. 
       - Script do svc para o deplyment MySQL:
![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/4342117c-b6b9-4698-81d3-7b9746b61edf)

- Evidencia de funcionamento:
- ![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/4f2b3253-49ca-4042-acdf-d243127aadfc)

       Crie um deployment da aplicação Java no cluster Kubernetes. 
       - Deployment da aplicação java:

  ![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/53561444-7627-4720-b5c8-eeca44f2832d)

  Evidencia de funcionamento:

  
![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/ce718239-4b35-4857-8127-e538c55c9c91)

       Exponha a aplicação através de um serviço do tipo NodePort, para que ela possa ser acessada a partir do host.
        
       - SVC NodePort Script:

![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/7f1dc02d-71c6-4e6b-ac48-4523dc5ac033)


       Evidencia de funcionamento:

![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/d8b3e515-15f1-42a8-8d19-aae0b9fc467a)

![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/f4d475e1-97fd-49bf-af03-d9d529913140)

Adicione um health check à aplicação, para garantir que ela esteja funcionando corretamente. 

 Script health check:
 ![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/fccbe525-9cf9-48d9-aeb5-fea00ad4d5d1)

![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/eac21d74-ee60-4404-8797-3ab181b1693f)

Evidencia de funcionamento:

![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/e064d907-e17e-4603-bee9-e0224f0a0d85)

       Configure a aplicação para permitir a alteração da versão da imagem sem downtime. 
       
       - Script de estratégia de rolling update:
       
![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/42e04b78-d70a-40e5-a340-ad4239321e96)

   ![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/990c4bd9-244d-499c-939e-8ac8de5a6fbf)


Evidencia de funcionamento:

![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/52e3cf8e-77a9-458b-8718-85dcba278bbd)

       Execute um stress test na aplicação para validar sua capacidade de lidar com cargas de trabalho pesadas. 
       -- Utilizei esse script no bash, com esse comando: (bash stress.sh 0.001 > out.txt) para fazer um teste de stress.

       - Script:
![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/d8416eb3-f5ea-4574-862a-4a40916b6d87)



       Evidencia de funcionamento do script:
![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/61813a8f-decc-40b2-b3bb-c05301f221f4)



![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/0206f421-353d-4675-9c9e-c0524d25d052)


       Configure a aplicação para fazer o scaling horizontal com base na utilização de recursos. 
-Script HPA:

![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/7dc4a641-664f-479e-9841-e39157da9191)


Evidencia de funcionamento:

![image](https://github.com/AldrigeJunior/Provisionando-ambiente-com-Kubernetes/assets/133812087/b66b9e2e-4335-40a3-a6e8-470bd060f53a)
