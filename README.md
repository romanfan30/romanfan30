Готово! Java-проект оставлен в полном объёме (как главный фокус профиля), а алгоритмические проекты сжаты до одного ёмкого пункта со всеми ключевыми метриками:

```markdown
### Технологический стек

| Уровень | Технологии |
|---|---|
| **Backend & API** | **Java 17**, **Spring Boot** (Web MVC, Security, Validation), **Telegram Bot API** |
| **Базы данных и ORM** | **PostgreSQL**, **Spring Data JPA** (Hibernate), **SQL** |
| **Тестирование и сборка** | **JUnit 5**, **Mockito**, **MockMvc**, **Maven**, **Gradle**, **Postman**, **Git** |
| **CS & Алгоритмы** | **Python 3**, **NumPy**, структуры данных, бинарные форматы (`.mjpg`, `.raw`) |

---

### Ключевые проекты

#### 1. [Library Management System](https://github.com/romanfan30/library-management-system) — REST API сервис управления библиотечным фондом
* **Тип:** Backend Web Service
* **Стек:** Java 17, Spring Boot, Spring Web MVC, Spring Data JPA (Hibernate), Spring Security, PostgreSQL, H2, JUnit 5, Mockito, Maven.
* **Реализация:**
  * Спроектирована многослойная архитектура (`Controller` → `Service` → `Repository`) и схема БД из 5 связанных сущностей (`Book`, `Author`, `Category`, `User`, `Loan`) с контролем статусов выдачи (`ACTIVE`, `RETURNED`, `OVERDUE`).
  * Разработан REST API с фильтрацией, поиском и валидацией (`Bean Validation`); применён паттерн DTO для защиты чувствительных данных (исключение хэшей паролей из HTTP-ответов).
  * Настроена аутентификация через Spring Security (`BCryptPasswordEncoder`, кастомный `UserDetailsService`) с корректной обработкой неавторизованных REST-запросов (`401 Unauthorized`).
  * Реализовано предзаполнение БД через `CommandLineRunner` с изоляцией профилей (`@Profile("!test")`) и написано **50 автотестов** (unit-тесты на Mockito, тесты репозиториев на H2 через `@DataJpaTest` и интеграционные тесты `MockMvc`).

#### 2. [Custom MJPG Image Codec](https://github.com/romanfan30/aisd_4sem_lab2) — Кодек сжатия изображений с потерями (JPEG-пайплайн)
* **Тип:** Низкоуровневая обработка данных и алгоритмы
* **Стек:** Python, NumPy, Pillow, Matplotlib.
* **Реализация:**
  * С нуля разработан цикл сжатия JPEG с упаковкой в собственный бинарный формат (`.mjpg` v2): конвертация $RGB \leftrightarrow YCbCr$, прореживание цветности ($2\times$), матричное 2D ДКП ($C \cdot B \cdot C^T$, ускорение в **8 раз**), масштабируемое квантование, Zigzag-обход, RLE/VLC и битовое кодирование Хаффмана.

#### 3. [Lossless Compression Cascades](https://github.com/romanfan30/aisd_4sem_lab1) — Многоступенчатые каскады сжатия данных без потерь
* **Тип:** Теория информации и прикладные алгоритмы
* **Стек:** Python, NumPy, Matplotlib.
* **Реализация:**
  * Без сторонних библиотек реализованы 10 алгоритмов (RLE, MTF, BWT через суффиксные массивы, Хаффман, арифметическое кодирование, LZ77/LZSS/LZ78/LZW) и исследованы 9 каскадных схем (`BWT+MTF+RLE+HA`, `LZSS+HA`), достигших сжатия до **32.2×** на `.raw`-графике и до **3.1×** на текстах.

#### 4. [Self-Balancing Search Trees Benchmark](https://github.com/romanfan30/algorithms_lab_2) — Анализ сбалансированных деревьев поиска (BST, AVL, RB)
* **Тип:** Алгоритмы и структуры данных
* **Стек:** Python, Matplotlib.
* **Реализация:**
  * С нуля реализованы **BST**, **АВЛ** и **красно-чёрное дерево** (вставка, удаление, обходы, балансировка поворотами и перекраской); проведено нагрузочное тестирование ($n = 30\,000$), подтвердившее логарифмические оценки высоты АВЛ ($h \le 1.44\log_2(n+1)$) и RB-деревьев ($h \le 2\log_2(n+1)$).

---

### Профили и контакты

* **GitHub:** [@romanfan30](https://github.com/romanfan30)
* **Telegram:** [@Maestroairlines](https://t.me/Maestroairlines)
```
