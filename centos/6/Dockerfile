FROM toopher/centos-i386:centos6

RUN yum -y update &&\
    yum -y install vim\
                   wget\
                   gcc\
                   autoconf\
                   zlib-devel\
                   gettext\
                   asciidoc\
                   xmlto\
                   perl-ExtUtils-MakeMaker &&\
    yum clean all
RUN cd /tmp &&\
    wget http://www.kernel.org/pub/software/scm/git/git-2.7.4.tar.gz &&\
    tar xf git-2.7.4.tar.gz &&\
    cd /tmp/git-2.7.4 &&\
    make -j3 configure &&\
    ./configure --prefix=/usr &&\
    make -j3 all doc &&\
    make -j3 install install-doc install-html &&\
    rm -rf /tmp/git-2.7.4*

