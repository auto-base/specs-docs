# Спецификация публичного API проекта %product%

В данной статье рассматривается спецификация публичного API проекта %product%.

<tip>
    Вы также можете попробовать <a href="local-setup.md">локальный запуск</a>.
</tip>

## Публичное API

Публичное API проекта %product% доступно по <a href="https://auto-base.github.io/specs/">ссылке</a>.

При открытии публичной спецификации вы увидите интерфейс swagger-ui который позволяет выполнять запросы к публичному API проекта %product%.

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

