# Локальный запуск спецификации внешнего API проекта %product%

<tip>
    Вы также можете попробовать запуск из <a href="public-api.md">документации</a> 
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

## Установка Docker

Для локального запуска и отладки публичной спецификации API %product% вам может понадобиться Docker

<procedure>
    <step>Зайдите на <a href="https://docs.docker.com/get-started/get-docker/">официальный сайт docker</a> и установите последнюю версию для вашей ОС</step>
</procedure>

## Настройка переменных среды

Для локального запуска и отладки публичной спецификации API %product% вам также необходимо настроить переменные среды,
для этого:

<procedure title="Установка переменных среды" id="env_setup">
    <step>
        Перечень всех переменных сред используемых во внешней спецификации проекта %product%
        <table>
            <tr>
                <td>Переменная</td>
                <td>Значение</td>
            </tr>
            <tr>
                <td>SWAGGER_PORT</td>
                <td>Порт для swagger ui по умолчанию - 9096</td>
            </tr>
        </table>
    </step>
    <step>
        Установка обязательных параметров
        <tabs>
            <tab title="%windows%">
                <tip>Для установки переменных среды перманентно можете изучить данную <a href="windows-env.md">статью</a>, либо изучить <a href="https://superuser.com/a/1529193">данное обсуждение</a></tip>
                <p>Для установки переменных среды на ОС %windows%</p>
                <code-block lang="powershell">
                    set "SWAGGER_PORT=9096"
                </code-block>
            </tab>
            <tab title="%unix%">
                <tip>Для установки переменных среды перманентно можете изучить данную <a href="unix-env.md">статью</a></tip>
                <p>Для установки переменных среды на ОС %unix%</p>
                <code-block lang="bash">
                    export SWAGGER_PORT=9096
                </code-block>
            </tab>
        </tabs>
    </step>
</procedure>

## Локальный запуск спецификации

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