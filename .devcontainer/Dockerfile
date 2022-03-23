FROM pytorch/pytorch:latest

# Install required libraries
RUN conda config --add channels pytorch \
 && conda config --append channels conda-forge \
 && conda update --all --yes --quiet \
 && conda install --yes --quiet \
    ipywidgets \
    jupyterlab \
    matplotlib \
    nodejs \
    opencv \
    pandas \
    scikit-learn \
    seaborn \
    sympy \
 && conda clean --all -f -y
# aptパッケージの更新、エディタ(vim)のインストール
RUN apt update -y && apt upgrade -y && \
    apt install -y vim 
    
# python関連ライブラリのインストール
RUN pip install numpy matplotlib jupyter

# コンテナ起動時にbashを起動
CMD ["/bin/bash"]