# hw_keepalived
## Задание 1  
Дана схема для Cisco Packet Tracer, рассматриваемая в лекции.  
На данной схеме уже настроено отслеживание интерфейсов маршрутизаторов Gi0/1 (для нулевой группы)  
Необходимо аналогично настроить отслеживание состояния интерфейсов Gi0/0 (для первой группы).  
Для проверки корректности настройки, разорвите один из кабелей между одним из маршрутизаторов и Switch0 и запустите ping между PC0 и Server0.  
На проверку отправьте получившуюся схему в формате pkt и скриншот, где виден процесс настройки маршрутизатора.  
  ![ka1](https://github.com/neo-13th/hw_keepalived/assets/150372172/bd89d0bb-f7cf-4299-90e7-de07b4367cb6)  
  
![ka2](https://github.com/neo-13th/hw_keepalived/assets/150372172/e70e268d-15ee-42f8-bafb-e2d4e4e4edea)  

![ka3](https://github.com/neo-13th/hw_keepalived/assets/150372172/581020f9-bf58-4152-a2f7-81793861fb00)  

![ka5](https://github.com/neo-13th/hw_keepalived/assets/150372172/6c446044-85f0-458f-830f-c48f577a9fe2)  

![ka6](https://github.com/neo-13th/hw_keepalived/assets/150372172/91cf702e-7e3e-4aa3-b82b-06e8462fd56b)  

## Задание 2.
Запустите две виртуальные машины Linux, установите и настройте сервис Keepalived как в лекции, используя пример конфигурационного <a>файла</a>.  
Настройте любой веб-сервер (например, nginx или simple python server) на двух виртуальных машинах  
Напишите Bash-скрипт, который будет проверять доступность порта данного веб-сервера и существование файла index.html в root-директории данного веб-сервера.  
Настройте Keepalived так, чтобы он запускал данный скрипт каждые 3 секунды и переносил виртуальный IP на другой сервер, если bash-скрипт завершался с кодом, отличным от нуля (то есть порт веб-сервера был недоступен или отсутствовал index.html). Используйте для этого секцию vrrp_script  
На проверку отправьте получившейся bash-скрипт и конфигурационный файл keepalived, а также скриншот с демонстрацией переезда плавающего ip на другой сервер в случае недоступности порта или файла index.html  
Ссылка на скрипт https://github.com/neo-13th/hw_keepalived/blob/main/check.sh  
Ссылка на конфигурационный файл https://github.com/neo-13th/hw_keepalived/blob/main/keepalived.conf  

![kp1](https://github.com/neo-13th/hw_keepalived/assets/150372172/5ba04609-5150-40b9-a1d4-f41c7dae9f2f)  
![kp2](https://github.com/neo-13th/hw_keepalived/assets/150372172/7c8acd12-1add-4a68-b3d7-0b4013c6caae)  
![kp3](https://github.com/neo-13th/hw_keepalived/assets/150372172/6a61c478-d94e-4796-b09a-6dedf366efa9)  
После остановки сервиса на главной машине  
![kp4](https://github.com/neo-13th/hw_keepalived/assets/150372172/405aabee-0189-46a8-99d3-8e41fc676708)  








