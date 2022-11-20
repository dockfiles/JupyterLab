# JupyterLab

This docker-compose.yml will install [JupyterLab](https://jupyter.org/) and persist extensions you install to a [named volume](https://docs.docker.com/storage/volumes/).

# Requirements

- [Docker Engine](https://www.docker.com)
- [Docker Compose](https://docs.docker.com/compose/install/)

# Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/dockfiles/JupyterLab.git JupyterLab
```

cd into the new directory

```bash
cd JupyterLab
```

### 2. Run the container
```bash
docker compose up -d
```

### 3. Get the login token
After running the container, run
```bash
docker logs jupyter
```
![image](https://user-images.githubusercontent.com/110657529/202891031-1012895a-a411-44ad-918d-3249dec4d098.png)

Copy the token from the terminal

### 4. Login to JupyterLab
In a web browser, visit `http://localhost:10000`, and paste in the login token.

![image](https://user-images.githubusercontent.com/110657529/202891131-3b34002a-7688-4abf-b15d-a8d2ff0195a5.png)

### 5. Begin working 
Once logged in, you are able to use JupyterLab notebooks.
![image](https://user-images.githubusercontent.com/110657529/202891240-22ef3fbb-0204-4a30-b58e-66557b43334b.png)

Also notice that a `work` folder is created locally on your machine.
This folder is a bind mount to the `work` folder inside the container, and files you create in JupyterLab will persist to you local `work` folder.

![image](https://user-images.githubusercontent.com/110657529/202891336-70d1f683-0e7a-462a-909a-62146f603e0f.png)
