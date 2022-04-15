Bootstrap: docker
From: continuumio/miniconda

%post
apt-get --allow-releaseinfo-change update && DEBIAN_FRONTEND=noninteractive apt-get -y upgrade  && \
DEBIAN_FRONTEND=noninteractive apt-get -y install \
	libxxf86vm1
conda update conda && conda update --all
conda create -n cryolo -c conda-forge -c anaconda pyqt=5 python=3 numpy==1.18.5 libtiff wxPython=4.1.1  adwaita-icon-theme
eval "$(conda shell.bash hook)"
conda activate cryolo
pip install nvidia-pyindex
pip install 'cryolo[c11]'

%runscript
echo "initialising conda:"
eval "$(conda shell.bash hook)"
conda activate cryolo
