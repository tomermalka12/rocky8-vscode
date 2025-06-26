# 🔧 My Project Name

A short description of your project and what it does.

> Example: A Dockerized development environment for CentOS 7 with pre-installed VSCode Server, Git, and essential tools.

---

## 🚀 Features

- Pre-configured development environment
- Web-based VSCode access via browser
- Git + SSH setup for GitHub
- Easy-to-extend Dockerfile

---

## 📦 Technologies

- CentOS 7
- Docker
- code-server (VSCode in the browser)
- Git + SSH
- Bash / Shell

---

## 🖥️ Getting Started

### Prerequisites

- Docker installed
- GitHub account
- SSH key (see below)

### Clone the repository

```bash
git clone git@github.com:your-username/your-repo-name.git
cd your-repo-name
```

### Build and run the container

```bash
docker build -t my-dev-container .
docker run -it -p 8080:8080 -v $(pwd):/home/vscode/projects my-dev-container
```

Open [http://localhost:8080](http://localhost:8080) to access VSCode in the browser.

---

## 🔐 Setting up Git + SSH

1. Generate an SSH key (if you don’t have one):

    ```bash
    ssh-keygen -t ed25519 -C "your.email@example.com"
    ```

2. Add it to the agent:

    ```bash
    eval "$(ssh-agent -s)"
    ssh-add ~/.ssh/id_ed25519
    ```

3. Copy the public key:

    ```bash
    cat ~/.ssh/id_ed25519.pub
    ```

4. Add it to [GitHub SSH Keys](https://github.com/settings/keys)

---

## 🗃️ Project Structure

```
.
├── Dockerfile
├── README.md
├── .gitignore
├── projects/
│   └── example-code/
└── scripts/
    └── setup.sh
```

---

## 🤝 Contributing

Contributions, issues and feature requests are welcome!  
Feel free to open an issue or pull request.

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](./LICENSE) file for details.

---

## 👤 Authors

- **Tomer Malka Pinto** – [@tomermalka12](https://github.com/tomermalka12)
