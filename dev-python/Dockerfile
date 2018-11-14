FROM archaur

USER root

RUN pacman -Syu --noconfirm python-pip

USER archie
ENV PATH="${PATH}:/home/archie/.local/bin"

RUN pip install --user --upgrade pip
RUN pip install --user jedi flake8 autopep8 yapf

CMD /usr/bin/bash
