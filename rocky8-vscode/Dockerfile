FROM rockylinux:8

# Install dependencies
RUN yum install -y \
    curl \
    wget \
    tar \
    git \
    vim \
    sudo \
    passwd \
    gnupg2 && \
    yum clean all

# Create a user and set it without password
RUN useradd -m vscode && passwd -d vscode && usermod -aG wheel vscode

# Install code-server (VS Code in browser)
RUN curl -fsSL https://code-server.dev/install.sh | sh

# Expose code-server on port 8080
EXPOSE 8080

# Run code-server as vscode user
USER vscode
WORKDIR /home/vscode

# Run code-server without auth (only for private/dev use!)
CMD ["code-server", "--bind-addr", "0.0.0.0:8080", "--auth", "none"]


