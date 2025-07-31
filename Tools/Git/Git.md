**Содержание:**
* Команды
  * [Глобальные настройки](/Tools/Git/Git.md#%D0%B3%D0%BB%D0%BE%D0%B1%D0%B0%D0%BB%D1%8C%D0%BD%D1%8B%D0%B5-%D0%BD%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B8)
  * [Инициализация](/Tools/Git/Git.md#%D0%B8%D0%BD%D0%B8%D1%86%D0%B8%D0%B0%D0%BB%D0%B8%D0%B7%D0%B0%D1%86%D0%B8%D1%8F)
  * [Работа с файлами](/Tools/Git/Git.md#%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0-%D1%81-%D1%84%D0%B0%D0%B9%D0%BB%D0%B0%D0%BC%D0%B8)
  * [Коммиты](/Tools/Git/Git.md#%D0%BA%D0%BE%D0%BC%D0%BC%D0%B8%D1%82%D1%8B)
  * [Ветвление и слияние](/Tools/Git/Git.md#%D0%B2%D0%B5%D1%82%D0%B2%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B8-%D1%81%D0%BB%D0%B8%D1%8F%D0%BD%D0%B8%D0%B5)
  * [Работа с удалённым репозиторием](/Tools/Git/Git.md#%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%B0-%D1%81-%D1%83%D0%B4%D0%B0%D0%BB%D1%91%D0%BD%D0%BD%D1%8B%D0%BC-%D1%80%D0%B5%D0%BF%D0%BE%D0%B7%D0%B8%D1%82%D0%BE%D1%80%D0%B8%D0%B5%D0%BC)
  * [Полезные команды](/Tools/Git/Git.md#%D0%BF%D0%BE%D0%BB%D0%B5%D0%B7%D0%BD%D1%8B%D0%B5-%D0%BA%D0%BE%D0%BC%D0%B0%D0%BD%D0%B4%D1%8B)
  * [Просмотр информации](/Tools/Git/Git.md#%D0%BF%D1%80%D0%BE%D1%81%D0%BC%D0%BE%D1%82%D1%80-%D0%B8%D0%BD%D1%84%D0%BE%D1%80%D0%BC%D0%B0%D1%86%D0%B8%D0%B8)
* [Применение](/Tools/Git/Git.md#%D0%BF%D1%80%D0%B8%D0%BC%D0%B5%D0%BD%D0%B5%D0%BD%D0%B8%D0%B5)

---

### Глобальные настройки (.gitconfig)
> [!TIP]
> ```git config``` — команда для настройки параметров Git
> 
> ```--global``` — настройка применяется глобально для всех репозиториев текущего пользователя

Установка имени пользователя и его email, которые будут использоваться при фиксаций изменений (коммитов)
<pre>
git config --global user.name "Твоё Имя"
git config --global user.email "Твой email"
</pre>

Установка редактора кода по умолчанию
<pre>
git config --global core.editor "Твой редактор"
</pre>

Контроль преобразования CRLF ↔ LF (автоматическое преобразование строк и проверка безопасности преобразований)
<pre>
git config --global core.autocrlf true
git config --global core.safecrlf warn
</pre>

Отключение замены спец.символов (экранирования)
<pre>
git config --global core.quotepath off
</pre>

Установка основной ветки (main)
<pre>
git config --global init.defaultBranch main
</pre>

Cписок всех глобальных настроек
<pre>
git config --global --list
</pre>

