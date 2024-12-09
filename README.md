# Введение
Надеюсь после первой задачи вы научились отслеживать изменения файлов, а так же коммитить изменения.

Теперь давайте попробуем забрать из репозитория задачу выполненную другим разработчиком. В данном 
случае это будет очередной абзац нашего стихотворения

## Задание 

1. Из текущей ветки (dev-task_1) сознайте новую с именем состоящим из ваших ФИО, например *Vasia_Pupkin* это
   будет ваша основная ветка. От нее создайте еще одну ветку *task_1*
2. Добавьте в **index.html** первый абзац стихотворения
3. Выполните команду **git status**, обратите внимание на статус *modified* измененного файла
   Данный статус сообщает, что файл был изменен.
4. Создайте какой-либо файл и выполните **git status** еще раз, теперь вы должны увидеть,  
   что кроме *modified* git сообщает нам о *untracket files*, это означает, что этот файл   
   не отслеживается гитом
5. Добавьте ВСЕ изменения в коммит командой **git add -A**, выполните **git status**  
   обратите внимание, что все изменения готовы к коммиту *Changes to be committed*  
6. Внесите любую правку в свой тестовый, файл и проверьте статус **git status**,  
   теперь вы можете увидеть, что ваш файл отображается сразу в двух статусах.  
   Что бы добавить новые изменения к коммиту вам опять нужно выполнить **git add**  
   либо отменить ваши изменения командой **git checkout <nameFiles>** о чем вас проинформирует  
   консоль.  
   ***Важно отметить, что в коммит попадут только те изменения которые находятся в *staged* т.е.
   добавлены к коммиту. Очень важно контролировать изменения прикрепляемые к коммиту, так как 
   в него могут не попасть нужные изменения (вы забыли **git add**), либо попадут изменения 
   которых там быть не должно (например файлы пользователя)***
7. Попробуйте самостоятельно, добавлять файлы, вносить правки, добавлять к коммиту, сбрасывать изменения.
   Не бойтесь, что-либо сломать, это тренировка и она важна для понимания процессов.
8. Когда вы точно понимаете как управлять изменениями, создайте коммит **git commit** либо 
   **git commit -m <nameCommit>**, проверьте еще раз статус, там не должны отображаться изменения
   которые были добавленны к коммиту
9. Смержите основную ветку с веткой задачи, для этого перейдите в вашу основную ветку и выполните
   комманду git merge <name branch>, обязательно обратите внимание, что результатом вашего слияния
   стал новый коммит.
10. Отправьте ваши изменения в удаленный репозиторий **git push origin** где *origin* будет вашим
1. Из вашей основной ветки **name_surname**, создайте новую ветку **task_2** и перейдите в нее.
2. Выполните команду *git pull origin dev-task_2*. Вы заберете второй абзац стихотворения который
   имитирует задачу выполненную другим разработчиком.
3. В случае если у вас появились конфликты слияния, разрешите их.
4. Смержите ветку **task_2** с **name_surname**.
5. Результатом вашей работы должны быть 2 столбца стихотворения.
6. Отправьте ваши изменения в удаленный репозиторий **git push origin** где *origin* будет вашим
   удаленным репозиторием, сделайте pull request.


## Может понадобится
В результате работы у вас могут появляться файлы, которых не должно быть в репозитории
(например файлы среды разработки), для того что бы они не висели в *статусе* добавьте 
их в **.gitignore**. Просто создайте этот файл и запишите в нем файл или папку которы не должен
отслеживать git.
