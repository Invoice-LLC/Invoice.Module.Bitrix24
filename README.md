<h1>Invoice Payment Module</h1>

<h3>Установка</h3>

1. Перейдите в **Приложения -> Разработчикам**

<br> ![image](https://user-images.githubusercontent.com/91345275/230836938-d847c3dc-a000-4fcb-98fe-27b7e5d38570.png)<br> 

2. **Другое -> Локальное приложение**

3. Заполните данные:
 +  Выберите флажок **Серверное**
 +  Заполните поля **Путь вашего обработчика** и **Путь для первоначальной установки** как показано на скриншоте **`https://bitrix24.plugins.invoice.su/install.php`**
 +  Поставьте выберите **Использует только API**
 +  Настройте права, как показано на скриншоте **СRM, Сайты, Платёжные системы, Интернет-магазины**
 +  Нажмите **Сохранить**
 +  Скопируйте **Ключ приложения (client_secret)**, чтобы вставить его дальше в настройках платёжной системы
 
<br> ![image](https://user-images.githubusercontent.com/91345275/230838441-7dacfc73-a6d3-4809-884e-1654f0c70bd6.png)<br> 

4. Добавьте платёжную систему. Перейдите в **Сайты и магазины -> Платежи и доставка -> Платёжные системы -> Добавить платёжную систему**

<br> ![image](https://user-images.githubusercontent.com/91345275/230838675-067e3ebf-c023-4536-b058-48677c4fd3db.png)<br> 

<br> ![image](https://user-images.githubusercontent.com/91345275/230838986-9e9cd7e7-e547-45d1-8f05-a12c5d5433c9.png)<br> 

5. Заполните данные:
 +  Выберите из списка пользовательский обработчик invoice
 +  Введите заголовок и название
 +  Заполните **API_KEY, MERCHANT_ID, CLIENT_SECRET**.  api_key и merchant_id можно получить в [личном кабинете Invoice](https://lk.invoice.su/), CLIENT_SECRET в ранее созданом локальном приложении
 +  Нажмите **Сохранить**

<br>![image](https://user-images.githubusercontent.com/91345275/230841714-79f8ad3c-0c9d-47d3-a7b2-355487098610.png)<br>

6. Добавьте уведомление в личном кабинете Invoice(Вкладка Настройки->Уведомления->Добавить)
   с типом **WebHook** и адресом: **`https://bitrix24.plugins.invoice.su/invoicePaymentProcessor.php`**<br>
   ![Imgur](https://imgur.com/lMmKhj1.png)
   
7. Сделайте тестовую оплату