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
        <li><a href="#Лабораторная 3">Лабораторная 1</a></li>
      </ul>
    </li>
  </ol>
</details>


<a name="DEVOPS ЛАБЫ"></a>
# DEVOPS ЛАБЫ

<a name="Лабораторная 3"></a>
## Лабораторная 3

Нашей задачей было написать такой скрипт, чтобы при его пуше в гитхаб автоматически собирался докер образ и результат сборки сохранялся. Взяли докер файл из работы представленной для зачета по дополнительной дсциплине "DEVOPS" (основанной на voice changer ai).

Перед началом выполнения лабораторной работы был изучен **теоретический материал**, необходимый для данной ЛР. 

**Ход работы:**

При выполнении данной лабораторной работы мы использовали WSL, Docker и Github:

1. Взяли отдельный репозиторий и добавили в него директорию .github/workflows:
    ![dockerlab2](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/docklab2.png?raw=true)
   ![dockerfile](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/dockerfile.png?raw=true)

2. В контейнер взяли и добавили нужные строки, а в репозиторий добавили секретки, которые хранят имя пользователя и пароль от его DockerHub:
    
3. Создаем файл docker-push.yml в директории .github/workflows. В нем последовательно расписаны шаги выполнения скрипта: сменяем директорию на эту, осуществляем вход по заранее подготовленным секретам - имени пользователя и паролю в Docker Hub, затем собираем и пушим образ в гит:

   ![dockerlab](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/docklab.png?raw=true)

## Все готово! 
Образ появился в Docker hub а в гитхаб собрался workflow.
  
  ![Workflow](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/Workflow.png?raw=true)
  ![dockerfile](https://github.com/VsevolodLazebnyi/cloud-ict-2023/blob/main/add/dockerhub.png?raw=true)
