FROM archlinux/base

RUN pacman -Syuq --noconfirm git base-devel sudo namcap

RUN echo "Defaults        lecture = never" > /etc/sudoers.d/privacy \
    && echo "%wheel ALL=(ALL) NOPASSWD: ALL" > /etc/sudoers.d/wheel \
    && useradd -m -G wheel -s /bin/bash builder

USER builder
WORKDIR /home/builder
