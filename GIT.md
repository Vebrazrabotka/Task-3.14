[< К содержанию](readme.md):closed_book:

# Что такое Git и зачем он нужен?
***Git*** - это консольная утилита, для отслеживания и ведения истории изменения файлов, в вашем проекте. Чаще всего его используют для кода, но можно и для других файлов. Например, для картинок - полезно для дизайнеров.

С помощью **Git-a** вы можете откатить свой проект до более старой версии, сравнивать, анализировать или сливать свои изменения в репозиторий.

***Скачать программу GIT можно по ссылке*** :floppy_disk:  [скачать программу GIT](https://git-scm.com/) :open_file_folder:

---

## Репозиторий Git
:octocat:

**Репозиторием** называют хранилище вашего кода и историю его изменений. ***Git*** работает локально и все ваши репозитории хранятся в определенных папках на жестком диске.
:octocat:
Так же ваши репозитории можно хранить и в интернете. Обычно для этого используют три сервиса:

+ [GitHub](https://github.com/) ![](/GitHab.jpg)
   + [ ] GitHub :octocat: — это служба размещения в Интернете репозиториев Git, которые используются для хранения содержимого. В GitHub размещается основной репозиторий всех проектов. :octocat:
+ [Bitbucket](https://bitbucket.org/) ![](/Bitbucket.jpg)
   + [ ] Bitbucket (англ. Bit «бит» и Bucket «ведро») — веб-сервис для хостинга проектов и их совместной разработки, основанный на системе контроля версий Git.  По назначению и основным предлагаемым функциям аналогичен GitHub.
+ [GitLab](https://about.gitlab.com/) ![](/GitLab.jpg)
    + [ ] GitLab — это сайт и система управления репозиториями кода для Git. Также GitLab позволяет разработчикам вести непрерывный процесс развертывания для создания, тестирования и развертывания кода. 
  
---

**Ключ к пониманию** :key: :octocat:
Ключ к пониманию концепции **git** :octocat: — знание о «трех деревьях»:

  :white_check_mark: Рабочая директория — файловая система проекта (те файлы, с которыми вы работаете).
  :white_check_mark: Индекс — список отслеживаемых git-ом файлов и директорий, промежуточное хранилище изменений (редактирование, удаление отслеживаемых файлов).
  :white_check_mark: Директория `.git/` — все данные контроля версий этого проекта (вся история разработки: коммиты, ветки, теги и пр.).
Коммит — «сохранение» (хранит набор изменений, сделанный в рабочей директории с момента предыдущего коммита). Коммит неизменен, его нельзя отредактировать.

У всех коммитов (кроме самого первого) есть один или более родительских коммитов, поскольку коммиты хранят изменения от предыдущих состояний. 

---

***Указатели GIT***
- [X] `HEAD` — указатель на текущий коммит или на текущую ветку (то есть, в любом случае, на коммит). Указывает на родителя коммита, который будет создан следующим.
- [X] `ORIG_HEAD` — указатель на коммит, с которого вы только что переместили HEAD (командой `git reset ...`, например).
- [X] Ветка (`master, develop etc`.) — указатель на коммит. При добавлении коммита, указатель ветки перемещается с родительского коммита на новый.
- [X] Теги — простые указатели на коммиты. Не перемещаются. 
---

**Модели ветвления в GIT**

Существует множество способов применения git в проекте, а также сотрудничества с другими разработчиками. Помимо использования git для контроля версий кода вашего проекта, его можно использовать для координации того, как другие работают над проектом. Эффективнее всего этого можно достичь, применив какую-либо модель ветвления.

|   Модель ветвления  |   Когда использовать    |  Схема   |
|----------|:--------------:|-----------|
|1.Centralized Workflow| Идеально подходит для одиночного проекта. В своем проекте вы сможете использовать эту модель, для того чтобы видеть какие изменения произошли в течение процесса разработки. После проделанной работы вы коммитите изменения так, что позже сможете вернуться к любой из предыдущих версий. Также она отлично подойдет для небольших команд которые перешли от syn к git.|![](Centralized%20Workflow.jpg)|
|2. Developer Branch Workflow  :octocat:|Больше подойдет для небольшого проекта с ограниченным количеством требований и небольшим количеством разработчиков, которым нужно чтобы их изменения в проекте были просмотрены до слияния с веткой master. Допустим у вас групповое задание, каждый участник делает свою часть, а затем публикует её в удаленном репозитории для того чтобы остальные её увидели до того, как она будет слита.|![](/Developer%20Branch%20Workflow.jpg)|
|3. Feature Branch Workflow|Этот подход больше подходит командам, которые используют какой-то метод по управлению проектами(например Agile). Давайте скажем, что ваш проект находится в продолжительной разработке и вам нужно добавить набор фич до следующего релиза. Эти фичи назначены разным разработчикам, которые создают отдельную ветку для каждой опубликованной фичи до того, как она будет слита с dev для тестирования. Когда вы готовы к релизу, dev сливается с master.|![](/Feature%20Branch%20Workflow.jpg)|
|4. Forking Workflow  :octocat:|Чаще всего используется в проектах с открытым исходным кодом и публичными репозиториями. Каждый кто может просматривать репозиторий может сделать разветвление. До тех пор, пока они могут просматривать репозиторий им не нужен доступ для того чтобы внести изменения напрямую в репозиторий. Когда они закончили свою работу, они могут сделать запрос, который вы будете рассматривать и решите, что же с ним делать, интегрировать, отказать или просить доработать до окончательного слияния с проектом.|![](/Forking%20Workflow.jpg)|

