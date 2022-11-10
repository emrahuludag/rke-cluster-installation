RKE2 Kubernetes Cluster Installation

Hazırlamış olduğum dokümantasyon ile ansible kullanlarak 3 master 3 worker node'dan oluşan bir kubernetes cluster kurulumu yapacağız. Kurulum RHEL8 üzerinde gerçekleştireceğim. Kurulumda öncelikle tüm node'larda selinux ve swap kapatıyoruz. Daha sonra kubernetes network için konfigürasyonlar yapılacaktır. İlk master sunucu kurulumu yapılır diğer master ve worker'ların join olabilmesi için gerekli token'i elde edeceğim. Daha sonra sahip olduğumuz token ile diğer node'ların kurulumu yapılacaktır.

https://wiki.acikkaynakfikirler.com/tr/rancher/AnsibleRKE2ClusterKurulumu

How To Run

ansible-playbook main.yml -i inventory.ini


####

Node'u silmeniz gerekmesi durumunda sunucunuzdaki hazır script ile temizleyebilirsiniz. BKZ: https://docs.rke2.io/install/linux_uninstall/

 /usr/bin/rke2-uninstall.sh 

 rm -rf /usr/local/bin/kubectl
