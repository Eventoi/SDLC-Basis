**Содержание:**
* Команды
  * [Глобальные настройки](/Testing/Tools/Git/Git.md#%D0%B3%D0%BB%D0%BE%D0%B1%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%B5-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B8)
  * [Инициализация](/Testing/Tools/Git/Git.md#%D0%B8%D0%BD%D0%B8%D1%86%D0%B8%D0%B0%D0%BB%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F)
  * [Работа с файлами](/Testing/Tools/Git/Git.md#%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0-%D1%81-%D1%84%D0%B0%D0%B9%D0%BB%D0%B0%D0%BC%D0%B8)
  * [Коммиты](/Testing/Tools/Git/Git.md#%D0%BA%D0%BE%D0%BC%D0%BC%D0%B8%D1%82%D1%8B)
  * [Ветвление и слияние](/Testing/Tools/Git/Git.md#%D0%B2%D0%B5%D1%82%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B8-%D1%81%D0%BB%D0%B8%D1%8F%D0%BD%D0%B8%D0%B5)
  * [Работа с удалённым репозиторием](/Testing/Tools/Git/Git.md#%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0-%D1%81-%D1%83%D0%B4%D0%B0%D0%BB%D1%91%D0%BD%D0%BD%D1%8B%D0%BC-%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B5%D0%BC)
  * [Полезные команды](/Testing/Tools/Git/Git.md#%D0%BF%D0%BE%D0%BB%D0%B5%D0%B7%D0%BD%D1%8B%D0%B5-%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D1%8B)
  * [Просмотр информации](/Testing/Tools/Git/Git.md#%D0%BF%D1%80%D0%BE%D1%81%D0%BC%D0%BE%D1%82%D1%80-%D0%B8%D0%BD%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%86%D0%B8%D0%B8)
* Применение

---

### Глобальные настройки
> [!TIP]
> ```git config``` — команда для настройки параметров Git
> 
> ```--global``` — настройка применяется глобально для всех репозиториев текущего пользователя
> 
> ```--wait``` (на Unix) или ```-wait``` (на Windows) - обязательно, иначе редактор кода сразу закроется не дождавшись редактирования сообщения коммита
> 
> ```-multiInst``` - открывает новый экземпляр редактора кода, даже если уже есть открытые окна
> 
> ```-notabbar``` - скрывает панель вкладок, чтобы открыть только один файл (удобно для ввода коммита)
> 
> ```-nosession``` - не загружает последнюю сессию (отключает автозагрузку ранее открытых файлов)
> 
> ```-noPlugin``` - отключает загрузку всех плагинов при запуске (уменьшает помехи и ускоряет запуск)
> 
> ```C:/.../notepad++.exe``` - полный путь указывается, если не прописана системная переменная PATH

Установка имени пользователя и его email, которое будет использоваться при фиксаций изменений (коммитов)
<pre>
git config --global user.name "Твоё Имя"
git config --global user.email "Твой email"
</pre>

Установка редактора кода по умолчанию
<pre>
git config --global core.editor "Твой редактор"

Nano / Vim
git config --global core.editor "nano" / "vim"

VS Code
git config --global core.editor "code --wait"

Notepad++
git config --global core.editor "'C:/Program Files/Notepad++/notepad++.exe' -multiInst -notabbar -nosession -noPlugin -wait"
</pre>














git config --list      # Показать текущую конфигурацию\



git config --global core.autocrlf true # Правильный формат строк
git config --global core.safecrlf warn # Правильный формат строк
git config --global core.quotepath off # Установка правильной кодировки
git config --global init.defaultBranch main # Установка общепринятого названия основной ветки
git config --global --list # Просмотр списка глобальных настроек



---

### Инициализация
Инициализировать новый репозиторий
> git init

---

### Работа с файлами

git status             # Проверить статус репозитория
git add <файл>         # Добавить файл к индексации (staging)
git add .              # Добавить все изменения
git restore <файл>     # Отменить изменения в файле
git rm <файл>          # Удалить файл из индекса и из рабочей директории

---

### Коммиты

git commit -m "Сообщение"            # Сделать коммит
git commit -am "Сообщение"           # Добавить и закоммитить (только отслеживаемые файлы)
git log                              # История коммитов
git log --oneline --graph --all      # Визуально и кратко
git show <hash>                      # Показать изменения коммита

---

### Ветвление и слияние

git branch                           # Показать список веток
git branch <имя>                     # Создать новую ветку
git checkout <ветка>                 # Переключиться на ветку
git checkout -b <имя>                # Создать и переключиться на ветку
git merge <ветка>                    # Слить ветку в текущую
git branch -d <ветка>                # Удалить ветку

---

### Работа с удалённым репозиторием

git remote add origin <url>               # Привязать удалённый репозиторий
git remote -v                             # Показать удалённые репозитории
git push -u origin main                   # Отправить ветку и установить upstream
  git push --set-upstream origin main     # Отправить ветку и установить upstream (-u это то же самое, что и --set-upstream)
git push                                  # Отправить изменения
git pull                                  # Получить и слить изменения
git clone <url>                           # Клонировать репозиторий

---

### Полезные команды

git stash                                 # Спрятать незакоммиченные изменения
git stash pop                             # Вернуть спрятанные изменения
git diff                                  # Показать разницу в коде
git diff --staged                         # Разница для проиндексированных файлов
git reset <файл>                          # Убрать из индекса
git reset --hard                          # Откатить все изменения
git clean -fd                             # Удалить все неотслеживаемые файлы и каталоги

---

### Просмотр информации

git log --graph --decorate --oneline --all  # Визуальная история всех веток
git blame <файл>                            # Кто и когда изменил строки
git reflog                                  # История всех действий (включая удалённые коммиты)