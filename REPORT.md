<h3>Отчёт по лабораторной работы №4</h3>
<h4>Выполнил: Останин А.</h4>

1) Создадим Dockerfile и впишем в него инструкции для установки aafire и ping
   <br>![image](https://github.com/user-attachments/assets/06946f1c-321e-46c1-bff6-4eacaa860fd4)<br>
2) Создадим образ командой ```docker build -t aafire .```
   <br>![image](https://github.com/user-attachments/assets/af076ad6-2673-4cc1-98a3-4ced2733270e)<br>
3) Запустим 2 контейнера в разных окнах терминала от этого образа командой ```docker run -it aafire```
   <br>![image](https://github.com/user-attachments/assets/cee82d1f-fcf9-4d5d-b756-f98e4c8063e7) ![image](https://github.com/user-attachments/assets/f4eb1006-4289-482a-a99e-f5659b1f43bf) ![image](https://github.com/user-attachments/assets/82a87edf-2680-458d-b89a-17b3db792989)
<br>
4) Теперь создадим сеть командой ```docker network create MyNetwork``` и подключим к ней, запущенные ранее контейнеры командами ```docker network connect myNetwork goofy_goldstine``` и ```docker network connect myNetwork frosty_dhawan```
5) С помощью команды ```docker network inspect myNetwork``` убедимся, что контейнеры присоединились к сети
   <br>![image](https://github.com/user-attachments/assets/2adf9fa2-0636-4a6c-a18c-9743d58a2250)<br>
6) Протестируем соединения, используя ```ping``` и ip-адрес контейнеров
   <br>![image](https://github.com/user-attachments/assets/cb067ae7-68a4-42c1-a91d-d521a5eadd5b) ![image](https://github.com/user-attachments/assets/1a8ba7fb-b9df-4373-8f4d-0c87d2f9e2a4)<br>
всё работает.
<h4>Вывод</h4>
Мы научились создавать образы в Docker и запускать по ним контейнеры, а также соединять эти контейнеры через ip-адрес.
