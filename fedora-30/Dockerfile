FROM fedora:30

RUN dnf -y update \
 && dnf -y group install "Development Tools" "C Development Tools and Libraries"

RUN dnf -y install \
    redhat-rpm-config \
    python3 \
    python3-pip \
    python3-setuptools \
    python3-wheel \
    python3-cffi \
    python3-devel \
    libffi-devel \
    cairo \
    pango \
    gdk-pixbuf2 \
    unixODBC \
    unixODBC-devel \
    langpacks-pt_BR

RUN curl https://packages.microsoft.com/config/rhel/7/prod.repo > /etc/yum.repos.d/mssql-release.repo
RUN dnf -y update
RUN ACCEPT_EULA=Y dnf -y install msodbcsql17 mssql-tools
RUN echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bash_profile
RUN echo 'export PATH="$PATH:/opt/mssql-tools/bin"' >> ~/.bashrc
RUN source ~/.bashrc

RUN LANG=pt_BR.UTF-8

WORKDIR /application
