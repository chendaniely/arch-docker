FROM archaur

USER root

RUN pacman -Syu --noconfirm python-pip

USER archie
ENV PATH="${PATH}:/home/archie/.local/bin"

RUN pip install --user --upgrade pip
RUN pip install --user jedi flake8 autopep8 yapf black

RUN pip install --user ipython pandas numpy seaborn scikit-learn statsmodels
COPY install.el install.el
COPY .emacs .emacs
RUN emacs --script install.el

CMD /bin/bash
