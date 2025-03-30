# 🐳 Container Environment (`container-env`)

The **Container Environment (`container-env`)**  in the TOolinUp DevKit provides a provides essential containerization tools for WSL2. It includes **Docker, Podman, Buildah, and Skopeo**, allowing developers to build, manage, and run containers efficiently.

## 🚀 Features
✅ **Docker** – Industry-standard container runtime  
✅ **Docker Compose** – Define and run multi-container applications  
✅ **Podman** – A daemonless alternative to Docker  
✅ **Buildah** – Create OCI/Docker images without a daemon  
✅ **Skopeo** – Manage container images across different registries  

## 🛠 Installation

### **Prerequisites**
- You must have **WSL2 installed**. If not, first install `wsl-env`:  
  ```sh
  scoop install wsl-env
  ```
- Ensure you have added the **ToolinUp DevKit** bucket to Scoop:  
  ```sh
  scoop bucket add toolingup https://github.com/ToolinUp/DevKit.git
  ```

### **Install `container-env`**
```sh
scoop install container-env
```

### **Post-Installation Steps**
After installation, restart WSL:  
```sh
wsl --shutdown
```
Then verify Docker is working:  
```sh
docker version
```
To check Podman:  
```sh
podman info
```

## 🔥 Why Use `container-env`?
- 🐳 **Seamless Docker support in WSL2**
- ⚡ **Lightweight alternatives (Podman, Buildah, Skopeo) included**
- 🔄 **Runs containers efficiently inside WSL2**

## 🎯 Next Steps
- Try running a test container:  
  ```sh
  docker run hello-world
  ```
- Use **`docker-compose`** for multi-container applications  
- Explore **Podman** as a drop-in replacement for Docker  

For advanced setups, check out [ToolinUp DevKit Documentation](https://www.toolingup.com). 