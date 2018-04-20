# Сервис сокращения ссылок

Для сокращения ссылок используется шифрования id сущности Link.
Шифрования производится на основе словаря и библиотеки https://github.com/recyger/encry-int.git

# Установка
Клонирование репозитария
```
git clone --recursive https://github.com/recyger/shortner.git
```

Запуск сервиса
```
docker-compose up --build
```

# Использованиие
Зайти на сайт http://127.0.0.1:8080/ и в разделе `new Link` создать новую ссылку.
При детальном просмотре в поле `Shortener` будет представлена сжатая ссылка


# Что не сделано

* Выделение механизма сжатия в bundle и настрока через конфигурацию
* Использование множественных словарей, для повышения криптостойкости по функции ```hash(url) % n```. Где n это количество словарей.
* Представление статистики переходов по сокращенным ссылка
* Время жизни ссылок
* Выделение frond и backend приложений в отдельные сервисы
