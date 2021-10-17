## Решение
1. При помощи [Vagrantfile](https://github.com/Probablyall/12.4/blob/main/Vagrantfile) создал 5 виртуалок;
2. Настроил [ssh](https://myadventuresincoding.wordpress.com/2011/12/22/linux-how-to-ssh-between-two-linux-computers-without-needing-a-password/) между ними;
3. По [этой](https://github.com/kubernetes-sigs/kubespray) инструкции сформировал [hosts.yaml](https://github.com/Probablyall/12.4/blob/main/hosts.yaml);
4. В файле group_vars/k8s_cluster поменял параметр на container_manager: containerd;
5. Запустил команду ansible-playbook -i inventory/mycluster/hosts.yaml  --become --become-user=root cluster.yml.

В процессе выполнения запроса возникали различные ошибки, но все их поправил. Итого кластер не получилось поднять, т.к. мой ноутбук не справился (i5 восьмого поколения, 16Гб RAM, SSD) и виртуал бокс свалился с ошибкой.


По [другой](https://rebrainme.com/blog/kubernetes/sozdanie-klastera-kubernetes-na-vps-s-pomoshhyu-kubespray/) инструкции также пробовал, получилось создать [такой](https://github.com/Probablyall/12.4/blob/main/hosts.ini) конфиг. 
