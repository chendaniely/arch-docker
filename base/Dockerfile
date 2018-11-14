FROM base/devel

RUN pacman -Syyu wget sudo nano emacs --noconfirm
RUN useradd -ms /bin/bash archie

# gives archie user passwordless sudo
RUN passwd -d archie
RUN printf 'archie ALL=(ALL) ALL\n' | tee -a /etc/sudoers

USER archie
WORKDIR /home/archie

RUN wget https://aur.archlinux.org/cgit/aur.git/snapshot/aurman.tar.gz
RUN tar -zxvf aurman.tar.gz
RUN ls -alh

WORKDIR /home/archie/aurman
RUN ls -alh
RUN gpg --recv-keys 465022E743D71E39
RUN  makepkg -s --noconfirm

WORKDIR /home/archie/

CMD /bin/bash
