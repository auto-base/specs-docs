# Установка переменных среды в постоянное хранилище %unix%

<procedure id="env_install_unix">
    <step>
        Для установки переменных среды на постоянной основе вам необходимо:
        <tabs>
            <tab title="Linux">
                Открыть терминал с помощью сочетания клавиш <shortcut>CTRL+T</shortcut>
            </tab>
            <tab title="MacOS">
                Открыть терминал с помощью сочетания клавиш <shortcut>COMMAND+T </shortcut>
            </tab>
        </tabs>
    </step>
    <step>
        Для установки переменных среды на постоянной основе вам необходимо:
        <tabs>
            <tab title="Linux">
                Ввести в терминал команду:
                <code-block>
                    nano ~/.profile
                </code-block>
            </tab>
            <tab title="MacOS">
               Ввести в терминал команду:
                <code-block>
                    nano ~/.zprofile
                </code-block>
            </tab>
        </tabs>
    </step>
    <step>
        Вписать в этот файл название вашей переменной и её значение
                <code-block>
                    export $SWAGGER_PORT=9096
                </code-block>
    </step>
     <step>
            Перезапустить все активные терминалы
    </step>
</procedure>