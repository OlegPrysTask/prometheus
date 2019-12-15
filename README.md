# prometheus
prometheus example

1. vagrant up 
2. vagrant scp . master:/home/vagrant/
3. chmod +x provision.sh
4. ./home/vagrant/provision.sh 

5. open Grafana/Prometheus/AlertManager 
http://localhost:30001/
admin:admin
http://localhost:30002/graph
http://localhost:30003/#/alerts

6. Testcases:
a. kubectl delete pod kube-controller-manager-master
b. yum install stress && stress --cpu 2 --timeout 60
c. fulload() { dd if=/dev/zero of=/dev/null | dd if=/dev/zero of=/dev/null | dd if=/dev/zero of=/dev/null | dd if=/dev/zero of=/dev/null & }; fulload; read; killall dd
d.yum install sress-ng && stress-ng --vm-bytes $(awk '/MemAvailable/{printf "%d\n", $2 * 0.9;}' < /proc/meminfo)k --vm-keep -m 1

