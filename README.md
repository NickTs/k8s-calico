1. Создаем пользователя ansible (!!! дальше от этого пользователя будут выполняться все скрипты).

ansible-playbook -i ./hosts ./1_cretae_user.yaml

2. Инсталируем необходимое ПО

ansible-playbook -i ./hosts ./2_pacakge_install.yaml
ansible-playbook -i ./hosts ./2_1_containerd_install.yaml

3. Запускаем инициализацию кластера

ansible-playbook -i ./hosts ./3_cluster_init.yaml 

4. Подключаем воркеры

ansible-playbook -i ./hosts ./4_join_workers.yaml
