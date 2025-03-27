# Локальный запуск спецификации внешнего API проекта %product%

В данной статье рассматривается локальный запуск спецификации публичного API проекта %product%.

<tip>
    Возможно вы искали запуск из <a href="public-api.md">документации</a>.
</tip>

## Начало работы

Чтобы начать локальное использование публичной спецификации API проекта %product%, необходимо клонировать её репозиторий
%title%, для этого:

<procedure title="Клонирование репозитория" id="клонирование_репозитория">
<step>
    <p>Перейдите на <a href="https://github.com/auto-base/specs">официальную страницу репозитория</a> спецификации проекта %product%</p>
</step>
<step>
    <p>Скачайте репозиторий</p>
    <tabs>
        <tab title="Интерфейс командной строки">
            <p>Откройте терминал в нужной вам папке и введите туда эту команду:</p>
            <code-block lang="console">
                git clone https://github.com/auto-base/specs.git
            </code-block>
        </tab>
        <tab title="Графический интерфейс">
            <procedure id="клонирование_репозитория_графический_интерфейс">
                <step>
                    <p>Нажмите на зеленую кнопку Code</p>
                    <img src="initial-clone-procedure-button.png" alt="Зеленая кнопка code" border-effect="line"/>  
                </step>
                <step>
                    <p>В открывшемся окне нажмите на кнопку Download ZIP</p>
                    <img src="initial-clone-procedure-modal-view.png" alt="Окно загрузки" border-effect="line"/>  
                </step>
            </procedure>
        </tab>
    </tabs>
</step>
</procedure>

## Локальный запуск спецификации
<tabs>
   <tab title="Браузер">
        Для запуска в браузере вам необходимо открыть репозиторий, открыть файл pages/index.html в браузере.
    </tab>
   <tab title="Докер-контейнер">
        <tabs>
            <tab title="%windows%">
                <p>Для локального запуска на ОС %windows%</p>
                <p>Вам также понадобится дополнительно ПО в виде make, установить её на компьютер с ОС %windows% можно с помощью <a href="https://www.cygwin.com/install.html">CYGWIN</a>.</p>
                <p>После чего вы сможете запустить публичную спецификацию внешнего API следующей командой:</p>        
                <code-block lang="powershell">
                    make run-swagger
                </code-block>
            </tab>
            <tab title="Linux">
                <p>Для локального запуска на ОС Linux</p>
                <p>Установите make, используя команду:</p>
                <code-block lang="bash">
                    apt install make
                </code-block>
                После чего - выполните эту команду 
                <code-block lang="bash">
                    make run-swagger
                </code-block>
            </tab>
            <tab title="MacOS">
                <p>Для локального запуска на macOS</p>
                <p>Убедитесь, что у вас установлен Homebrew. Если его нет, вы можете установить его, выполнив следующую команду в терминале:</p>
                <code-block lang="bash">
                    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
                </code-block>
                <p>После установки Homebrew, установите make:</p>
                <code-block lang="bash">
                    brew install make
                </code-block>
                <p>Теперь вы можете запустить проект:</p>
                <code-block lang="bash">
                    make run-swagger
                </code-block>
            </tab>
        </tabs>
    </tab>
</tabs>
<img src="swagger-ui-result.png" alt="Результат открытия документации" width="700"/>

## Авторизация

<procedure title="Для авторизации в публичном API проекта %product% необходимо:" id="для_авторизации_в_публичном_api_проекта_product_необходимо_">
<step>
    Нажать на зеленую кнопу Authorize
    <img src="authorize-swagger-ui-button.png" alt="Зеленая кнопка авторизации в swagger-ui"/>
</step>
<step>
    Ввести свои данные в форму basicAuth (http, Basic)
    <img src="authorize-swagger-ui-basic-auth-form.png" alt=""/>
</step>
<step>
    Нажать на зеленую кнопу Authorize
    <img src="authorize-swagger-ui-button-result.png" alt="Зеленая кнопка авторизации в swagger-ui"/>
</step>

После данных манипуляций вы сможете проводить запросы к публичному API проекта %product%.
Авторизация в публичном API проекта %product% обеспечивается через метод basic, суть которого заключается в подстановке пары значений логин:пароль.
</procedure>

<tip>
    Вы также можете попробовать запуск из <a href="public-api.md">документации</a>.
</tip>