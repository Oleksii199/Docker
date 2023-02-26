# Docker
#Удалите старые версии Docker (необязательно):
sudo apt-get remove docker docker-engine docker.io containerd runc

#Установите зависимости, которые позволят использовать репозиторий через HTTPS:
sudo apt-get update
sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg-agent \
    software-properties-common

#Добавьте ключ GPG официального репозитория Docker в вашу систему:
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

#Добавьте официальный репозиторий Docker в список источников пакетов:
sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

#Обновите список пакетов и установите последнюю версию Docker CE (Community Edition):
sudo apt-get update
sudo apt-get install docker-ce docker-ce-cli containerd.io

#Проверьте, что Docker установлен и работает, запустив команду:
sudo docker run hello-world


#Эта команда загрузит небольшой Docker-образ, запустит его в контейнере и выведет сообщение о том, что Docker работает правильно.

#Установка Docker на другие операционные системы (например, macOS или Windows) производится с использованием других инструкций. Более подробную информацию можно найти на официальном сайте Docker: https://docs.docker.com/get-docker/
