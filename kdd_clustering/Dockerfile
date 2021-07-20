FROM ubuntu:18.04

RUN apt-get update && apt-get install -y --no-install-recommends\
	apt-utils \
	build-essential \
	cmake \
	git \
	curl \
	python3 \
	python3-dev \
	python3-pip \
	python3-setuptools \
	python3-wheel \
	pandoc \
	texlive-xetex \
	texlive-fonts-recommended \
	texlive-generic-recommended


RUN pip3 install numpy \
	matplotlib \
	jupyter \
	pandas \
	sklearn \
	nbconvert

RUN mkdir kdd_clustering

EXPOSE 8888

CMD ["jupyter", "notebook", "--allow-root", "--notebook-dir=/kdd_clustering", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--NotebookApp.token=kdd"]
