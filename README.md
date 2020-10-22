# reproducibility-tutorial
FOSS 2020 tutorial

## Set-up commands
'''
    #download the Miniconda installer
    wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

    # instal miniconda silently (-b) in path (-p) /opt/conda
    bash Miniconda3-latest-Linux-x86_64.sh -b -p /opt/conda

    #make sure all conda packages will be in path by symbolic links to /bin
    ln -s /opt/conda/pkgs/*/bin/* /bin
    ln -s /opt/conda/bin/* /bin
    ln -s /opt/conda/pkgs/*/lib/* /usr/lib

    # Install Jupyter lab version 1.2.3
    /opt/conda/bin/conda install -c conda-forge -y jupyterlab=1.2.3
    /opt/conda/bin/conda install -c conda-forge -y nodejs=10.13.0

    python3 -m pip install bash_kernel
    pip install ipykernel
    python3 -m bash_kernel.install

    /opt/conda/bin/conda install -c conda-forge -y numpy geopandas pygeoprocessing

    #Test Jupyterlab
    jupyter lab --no-browser --allow-root --ip=0.0.0.0 --NotebookApp.token='' --NotebookApp.password='' --notebook-dir='/scratch/reproducibility-tutorial/'

    #Install Snakemake
    /opt/conda/bin/conda install -c bioconda -c conda-forge -y snakemake=5.8.1

    #install Docker
    # update ubuntu apt-get package manager
    sudo apt-get update

    # install some needed packages
    sudo apt-get install -y \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

    # add the Docker key
    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

    #add the repository
    sudo add-apt-repository \
     "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
     $(lsb_release -cs) \
     stable"

    # update apt-get with new repository information
    sudo apt-get update

    # install docker
    sudo apt-get install -y docker-ce docker-ce-cli containerd.io

    #test docker
    docker run hello-world

'''
