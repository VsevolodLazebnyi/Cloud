<a name="Вернуться в начало"></a>

<div align="center">

  <h3>Лабораторные работы команды "На тоненьком"</h3>
  <h4>по дисциплине: "Облачные технологии и услуги"</h4>

<div align="center">
  
```
    Состав команды:
  
    Боровский Максим (@unf1x)
    
    Лазебный Всеволод (@vllazebnyi)
```

<div align="left">


<details>
  <summary> Навигация </summary>
  <ol>
    <li>
      <a href="#DEVOPS ЛАБЫ">DEVOPS ЛАБЫ</a>
      <ul>
        <li><a href="#Лабораторная 1">Лабораторная 1</a></li>
        <li><a href="#Лабораторная 1* (со звездочкой)">Лабораторная 1* (со звездочкой)</a></li>
      </ul>
    </li>
  </ol>
</details>


<a name="DEVOPS ЛАБЫ"></a>
# DEVOPS ЛАБЫ

<a name="Лабораторная 1"></a>
## Лабораторная 1

```
Пользуясь терминалом на компьютере А перенести файл с компьютера Б на компьютер С,
находящиеся в одной локальной сети.

Понадобится ssh. Просьба использовать MacOS/Linux/WSL.
```

Перед началом выполнения лабораторной работы был изучен **теоретический материал**, необходимый для данной ЛР. 

``` ifconfig ``` - Пакет который мы скачали. По команде  ifconfig показывает ip adress, который понадобится нам для работы.

**Ход работы:**

При выполнении данной лабораторной работы мы использовали две системы WSL и одну VirtualBox(Ubuntu) машину:

   ![lab1.1](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/lab1.1.jpg?raw=true)

WSL Добавил на наши основные компьютеры подсистему Linux(Ubuntu) для Windows.
Между двумя компьютерами и виртуальной машиной "linuxvmvllazebnyi" настроили такой тип связи как сетевой мост, что гарантировало бы подключение к одной сети.

1. Скачали пакет sudo ifconfig. 
Нашли IP через терминал системы Linux с помощью команды ifconfig.
<div align="center">
  
```
    IP maks1m@: 172.28.7.52
    IP vllazebnyi@: 172.20.0.252
    IP linuxvmvllazebnyi@: 172.20.0.255
```

<div align="left">
  
3. Затем подключаемся к виртуальной машине "linuxvmvllazebnyi" и через неё перекидываем файл на подсистему “maks1m”. 
С использованием команд: 
``` ssh*username*@*ip* ``` и  ``` scp*username1*@*ip*:~*path* *username2*@*ip*:~*path* ```

   ![lab1.2](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/lab1.2.jpg?raw=true)

4. Перекинули в обратную сторону (через виртуальную машину на WSL “vllazebnyi”, пользуясь теми же командами:

 ![lab1.3](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/lab1.3.jpg?raw=true)
  
<a name="Лабораторная 1* (со звездочкой)"></a>
## Лабораторная 1* (со звездочкой)

```
Дополнить лабораторную работу 1, использовать публичные и приватные ключи (не логин и пароль)
```

``` ssh-keygen ``` - используется для создания пары SSH-ключей, которая состоит из приватного и публичного ключей. SSH-ключи представляют собой безопасный способ аутентификации при подключении к удаленному серверу через протокол SSH

``` ssh-copy-id ``` - используется для упрощения процесса копирования публичного ключа

---
**Ход работы:**

1. Берем главный компьютер “vllazebnyi” и генерируем ssh-ключ при помощи команды
``` ssh-keygen -t rsa ```
(Мы взяли уже существующий ключ для Git Bash и скопировали его в подсистему)

 ![lab1.4](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/lab1.4.jpg?raw=true)

  ![lab1.5](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/lab1.5.png?raw=true)



3. Далее копируем shh ключ на другое устройство
``` ssh-copy-id *username@ip* ```
  ![lab1.6](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/lab1.6.png?raw=true)



## Все готово!


