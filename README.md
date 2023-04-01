devops-netology

Из коммитов будут исключены файлы с расширениями .tfstate, .tfstate., .tfvars, .tfvars.json, .terraformrc;
будут исключены конкретные файлы crash.log, crash.*.log, override.tf, override.tf.json, terraform.rc; 
файлы имеющие окончание наименования _override.tf  _override.tf.json;
а так же будут исключены все файлы в субдиректориях **/.terraform/

## Задание

В клонированном репозитории:

1. Найдите полный хеш и комментарий коммита, хеш которого начинается на `aefea`. 

  > `git show aefea` - commit aefead2207ef7e2aa5dc81a34aedf0cad4c32545, Update CHANGELOG.md

  ![](https://github.com/Dmitriy-Chemezov/devops-netology/blob/main/0.png)

3. Ответьте на вопросы.

* Какому тегу соответствует коммит `85024d3`?

  > `git show 85024d3` - commit 85024d3100126de36331c6982bfaac02cdab9e76 (tag: v0.12.23)
  ![](https://github.com/Dmitriy-Chemezov/devops-netology/blob/main/1.png)

* Сколько родителей у коммита `b8d720`? Напишите их хеши.

  > `git show --pretty=format:' %P' b8d720`
  > Ответ - 56cd7859e05c36c06b56d013b55a252d0bb7e158  9ea88f22fc6269854151c571162c5bcf958bee2b

* Перечислите хеши и комментарии всех коммитов, которые были сделаны между тегами  v0.12.23 и v0.12.24.

  > `git log v0.12.23..v0.12.24 --oneline`
  ![](https://github.com/Dmitriy-Chemezov/devops-netology/blob/main/2.png)

* Найдите коммит, в котором была создана функция `func providerSource`, её определение в коде выглядит так: `func providerSource(...)` (вместо троеточия перечислены аргументы).

  > `git log -S 'func providerSource'`
 
  > Нашли два коммита:
  
  > commit 5af1e6234ab6da412fb8637393c5a17a1b293663
Author: Martin Atkins <mart@degeneration.co.uk>
Date:   Tue Apr 21 16:28:59 2020 -0700
  
  > commit 8c928e83589d90a031f811fae52a81be7153e82f
Author: Martin Atkins <mart@degeneration.co.uk>
Date:   Thu Apr 2 18:04:39 2020 -0700
  
  > Подробнее рассмотрим более ранний коммит
  
  > `git show 8c928e8 | grep "func providerSource"`
  
  > Получили ответ:  +func providerSource(services *disco.Disco) getproviders.Source {

* Найдите все коммиты, в которых была изменена функция `globalPluginDirs`.

  

* Кто автор функции `synchronizedWriters`? 

*В качестве решения ответьте на вопросы и опишите, как были получены эти ответы.*
