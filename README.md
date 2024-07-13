# New-docker-installation-setup

This documentation about docker
Author : HackBugs

Documentation : All About docker installation And setup and how to configure
----------------------------------------------------------------------------------
1 - Devops:
-------------

https://app.eraser.io/workspace/5bTzpbKkfb3PdcgYZ4Je

- In devops same like a datagard mean we make replica and duplicate of production database
same like we make replica and duplicate make make of aur environments where development working
we can make a container and of that container we can mutiple replicas and can share of each new deveploper 

- That means I want to work on a project where more than 50 or 100 programmers are working together. If 50 new people join the company, they will want to work on that project and start creating code. However, before writing code, they need to set up the required environment for that technology. For example, if I need to set up Android Studio for developing an application, the issue could arise if my teammates are using an older version of Android Studio. When I install Android Studio, it might be the latest version, and trying to run the project code could result in errors due to version differences. Additionally, my team might be using different operating systems like macOS, Linux, or Windows, which can also lead to environment setup errors.

Thats why we use of "Docker"

"Docker image and docker container"
Docker "image" is like class and docker "container" like object

Simple real prectical example of docker container and docker image
- Docker image means operation system it could be ubuntu or linux or mac anything only OS
- Docker container is act like virtual mechine not exctly vitual machine bec virtual machine is occupied more storage and container 
occupied less but is work same like virtual machine container is environment where i can install os, packeges, softwars etc which we 
install on one operating system

with docker can build the container
and of container we can make duplicate containers like local environment
and can use of that container to build and deploy projects without environment issues
------------------------------------------------------------------------------------------------
FROM ubuntu

RUN apt-get update
RUN apt-get install -y curl
RUN curl -sL https://deb.nodesource.com/setup_18.x | bash -
RUN apt-get upgrade -y
RUN apt-get install -y nodejs

COPY package.json package.json
COPY package-lock.json package-lock.json
COPY main.js main.js

RUN npm install

ENTRYPOINT [ "node", "main.js" ]
------------------------------------------------------------------------------------------------
Container or virtual machine manager, such as: 
Docker, QEMU, Hyperkit, Hyper-V, KVM, Parallels, Podman, VirtualBox, or VMware Fusion/Workstation
------------------------------------------------------------------------------------------------

2 - Kubernetes:
----------------

Chaliye, main aapko DevOps tools jaise Git, GitHub, Docker, kubectl, Minikube, Jenkins, Terraform, Prometheus, aur Grafana ka istemal kyun hota hai, usko real-life company examples ke through samjhata hoon:

### Real-Life Examples in Hinglish:

1. **Git & GitHub**:
   - **Use**: Version control system (Git) aur remote repositories (GitHub) jo code management ko organize aur collaborate karta hai.
   - **Example**: Ek software company jahan multiple developers ek project pe kaam kar rahe hain. Har developer apne changes ko Git mein commit karke push karta hai, jisse team ke members collaboration kar sake aur history track kar sake.

2. **Docker**:
   - **Use**: Containerization platform jo applications ko consistent environment mein run karne mein madad karta hai.
   - **Example**: Ek e-commerce company jo apne applications ko Docker containers mein deploy karke manage karti hai. Har new feature ya update ko separate containers mein test karne ke baad production environment mein deploy karti hai, jisse deployments reliable aur scalable hote hain.

3. **kubectl & Minikube**:
   - **Use**: Kubernetes cluster management (kubectl) aur local Kubernetes cluster setup (Minikube).
   - **Example**: Ek cloud services provider jahan har developer apne local machine pe Minikube se Kubernetes clusters setup karta hai. Developers kubectl se pods aur services ko manage karte hain, jo seamless aur consistent development experience provide karta hai.

4. **Jenkins**:
   - **Use**: Automation server jo CI/CD pipelines ko manage karta hai.
   - **Example**: Ek technology company jahan Jenkins pipelines code ko automatically build, test, aur deploy karte hain. Jab bhi koi developer code commit karta hai, Jenkins automatically build process ko trigger karta hai, tests run karta hai, aur code ko staging ya production environment mein deploy karta hai.

5. **Terraform**:
   - **Use**: Infrastructure as Code (IaC) tool jo infrastructure resources ko manage karta hai.
   - **Example**: Ek cloud solutions provider jahan infrastructure ko automate kiya jata hai Terraform ke through. Developers infrastructure resources ko Terraform scripts se define karte hain, jisse scaling, provisioning, aur management simplify hota hai.

6. **Prometheus & Grafana**:
   - **Use**: Monitoring aur metrics visualization tools.
   - **Example**: Ek financial services company jahan Prometheus metrics collect karta hai aur Grafana dashboards use hoti hain performance monitoring ke liye. Operations team realtime analytics aur alerts ke through infrastructure performance track karti hai, jisse issues early detection aur resolution hota hai.

Yeh examples dikhate hain ki DevOps tools ka istemal kaise companies apne development, deployment, aur infrastructure management processes ko automate aur streamline karne ke liye karte hain. In tools ki madad se teams efficient collaboration, reliable deployments, aur scalable infrastructure achieve karte hain. Agar aapko aur koi specific tool ya example ke baare mein jaanna hai, toh bataiye!