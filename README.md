# Домашнее задание:  Мосты, туннели и VPN


1. Настроить VPN между двумя ВМ в tun/tap режимах, замерить скорость в туннелях, сделать вывод об отличающихся показателях

   Vagrantfile + vpn.yml

    - Измерение скорости в режме TAP

![Image alt](https://github.com/AlexndrVakulenko/homework23/blob/main/01_Server_%D1%81%D0%BA%D0%BE%D1%80%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20%D1%82%D1%83%D0%BD%D0%BD%D0%B5%D0%BB%D0%B5_%D1%80%D0%B5%D0%B6%D0%B8%D0%BC_TAP.png)

![Image alt](https://github.com/AlexndrVakulenko/homework23/blob/main/03_Client_%D1%81%D0%BA%D0%BE%D1%80%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20%D1%82%D1%83%D0%BD%D0%BD%D0%B5%D0%BB%D0%B5_%D1%80%D0%B5%D0%B6%D0%B8%D0%BC_TAP.png)

    - Измерение скорости в режме TUN

![Image alt](https://github.com/AlexndrVakulenko/homework23/blob/main/02_Server_%D1%81%D0%BA%D0%BE%D1%80%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20%D1%82%D1%83%D0%BD%D0%BD%D0%B5%D0%BB%D0%B5_%D1%80%D0%B5%D0%B6%D0%B8%D0%BC_TUN.png)

![Image alt](https://github.com/AlexndrVakulenko/homework23/blob/main/04_Client_%D1%81%D0%BA%D0%BE%D1%80%D0%BE%D1%81%D1%82%D1%8C%20%D0%B2%20%D1%82%D1%83%D0%BD%D0%BD%D0%B5%D0%BB%D0%B5_%D1%80%D0%B5%D0%B6%D0%B8%D0%BC_TUN.png)

        Видим, что скорость в туннеле в режиме TUN чуть выше.




2. Поднять RAS на базе OpenVPN с клиентскими сертификатами, подключиться с локальной машины на ВМ

        Задание выполнялось на том же стенде с Vagrantfile. Ansible workbook vpn2.yml устанавливает необходимый софт на vm.
        Передаваемыйе файлы с сервера на клиент - в папке VPN_files/2

        Настройка сервера:
   
   ![Image alt](https://github.com/AlexndrVakulenko/homework23/blob/main/05_RAS_%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B01.png)

   ![Image alt](https://github.com/AlexndrVakulenko/homework23/blob/main/06_RAS_%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B02.png)

   ![Image alt](https://github.com/AlexndrVakulenko/homework23/blob/main/07_RAS_%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B03.png)

   ![Image alt](https://github.com/AlexndrVakulenko/homework23/blob/main/08_RAS_%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B04.png)

   ![Image alt](https://github.com/AlexndrVakulenko/homework23/blob/main/09_RAS_%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0_%D1%81%D0%B5%D1%80%D0%B2%D0%B5%D1%80%D0%B05.png)

         Настройка клиента:

  ![Image alt]( https://github.com/AlexndrVakulenko/homework23/blob/main/10_RAS_%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0_%D0%BA%D0%BB%D0%B8%D0%B5%D0%BD%D1%82%D0%B02.png)


            Подключение с помощью: ***жирный курсив*** openvpn --config client.conf

  ![Image alt]( https://github.com/AlexndrVakulenko/homework23/blob/main/11_RAS_%D0%A1%D0%B5%D1%81%D1%81%D0%B8%D1%8F_openVPN.png)

  ![Image alt](https://github.com/AlexndrVakulenko/homework23/blob/main/12_%D1%81%D0%B5%D1%82%D1%8C_%D1%82%D1%83%D0%BD%D0%BD%D0%B5%D0%BB%D1%8F.png)
