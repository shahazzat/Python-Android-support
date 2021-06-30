```
whereis python
 python3.8 --version
[root@localhost workspace]# python3.8 -m venv envdev
# Better to have 25GB disk space.
(envdev) [root@localhost workspace]# df -h
Filesystem               Size  Used Avail Use% Mounted on
devtmpfs                 1.2G     0  1.2G   0% /dev
tmpfs                    1.2G     0  1.2G   0% /dev/shm
tmpfs                    1.2G  8.6M  1.2G   1% /run
tmpfs                    1.2G     0  1.2G   0% /sys/fs/cgroup
/dev/mapper/centos-root   27G  2.3G   25G   9% /
vboxshare                246G  208G   39G  85% /root/shared
/dev/sda1               1014M  189M  826M  19% /boot
vboxshare                246G  208G   39G  85% /media/sf_vboxshare
tmpfs                    235M     0  235M   0% /run/user/0

(envdev) [root@localhost workspace]# . envdev/bin/activate
(envdev) [root@localhost workspace]# pip install ansible
(envdev) [root@localhost workspace]# ansible-playbook ~/shared/ansible_install_docker.yml
(envdev) [root@localhost workspace]# docker --version
(envdev) [root@localhost workspace]# git clone https://github.com/beeware/Python-Android-support.git
 cd Python-Android-support/
(envdev) [root@localhost Python-Android-support]# sh main.sh -v 3.8

------Error------
which: no shasum in (/home/shahazzat/workspace/envdev/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/root/bin)
Missing dependency: shasum

Please install it. One of following might work, depending on your system:

$ sudo apt-get install shasum
$ brew install shasum

Exiting.

Fix:
yum install -y perl-Digest-SHA
--------------
Change SHA
#    download xz "https://tukaani.org/xz/xz-5.2.5.tar.gz" "f6f4910fd033078738bd82bfba4f49219d03b17eb0794eb91efbae419f4aba10"
    download xz "https://tukaani.org/xz/xz-5.2.5.tar.gz" "251a85b3bac687974f360d3796048c20ded3bf0bd69e0d1cfd1db23d013f89ed"

Error:
Unable to access xz-src file or directory.
Download it by below command and replace existing from download folder:
(envdev) [root@localhost download]# wget https://tukaani.org/xz/xz-5.2.5.tar.gz
```
