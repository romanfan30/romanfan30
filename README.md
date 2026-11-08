### Технологический стек

| Уровень | Технологии |
|---|---|
| **Backend & API** | **Java 17**, **Spring Boot** (Web MVC, Security, Validation), **Telegram Bot API** |
| **Базы данных и ORM** | **PostgreSQL**, **Spring Data JPA** (Hibernate), **H2**, **SQL** |
| **Тестирование и инфра** | **Docker**, **JUnit 5**, **Mockito**, **MockMvc**, **Maven**, **Gradle**, **Postman**, **Git** |
| **CS & Алгоритмы** | **Python 3**, **NumPy**, структуры данных, бинарные форматы (`.mjpg`, `.raw`) |

---

### Ключевые проекты

#### 1. [Library Management System](https://github.com/romanfan30/library-management-system) — REST API управления библиотекой
* **Стек:** Java 17, Spring Boot, Spring Security, Spring Data JPA (Hibernate), PostgreSQL, H2, JUnit 5, Mockito, Maven.
* **Реализация:**
  * Спроектирована многослойная архитектура (`Controller` → `Service` → `Repository`) и схема БД из 5 сущностей (`Book`, `Author`, `Category`, `User`, `Loan`) со статусами выдачи (`ACTIVE`, `RETURNED`, `OVERDUE`).
  * Разработан REST API (CRUD, поиск по названию, фильтр доступных книг) с валидацией (`Bean Validation`); пароли не попадают в ответы благодаря DTO.
  * Настроена аутентификация на Spring Security: `BCrypt`, `UserDetailsService`, `401 Unauthorized` вместо редиректа на форму логина.
  * Написано **50 автотестов**: unit (`Mockito`), интеграционные (`@SpringBootTest` + `MockMvc`), репозиториев на H2 (`@DataJpaTest`).
 
  
#### 2. [Custom MJPG Image Codec](https://github.com/romanfan30/aisd_4sem_lab2) — Кодек сжатия изображений (JPEG-пайплайн)
* **Стек:** Python, NumPy, Pillow, Matplotlib.
* **Реализация:**
  * С нуля разработан JPEG-кодек со своим бинарным форматом (`.mjpg`): конвертация $RGB \leftrightarrow YCbCr$, прореживание цветности ($2\times$), матричное 2D ДКП (ускорение в **8 раз**), квантование, Zigzag, RLE/VLC и кодирование Хаффмана.

#### 3. [Lossless Compression Cascades](https://github.com/romanfan30/aisd_4sem_lab1) — Каскады сжатия данных без потерь
* **Стек:** Python, NumPy, Matplotlib.
* **Реализация:**
  * Без сторонних библиотек реализованы 10 алгоритмов (RLE, MTF, BWT, Хаффман, арифметическое кодирование, LZ77/LZSS/LZ78/LZW) и 9 каскадных схем (`BWT+MTF+RLE+HA`, `LZSS+HA`), дающих сжатие до **32.2×** на графике и **3.1×** на текстах.

#### 4. [Self-Balancing Search Trees Benchmark](https://github.com/romanfan30/algorithms_lab_2) — Анализ деревьев поиска (BST, AVL, RB)
* **Стек:** Python, Matplotlib.
* **Реализация:**
  * Реализованы **BST**, **АВЛ** и **красно-чёрное дерево** (вставка, удаление, 4 обхода, балансировка поворотами и перекраской); на выборке $n = 30\,000$ экспериментально подтверждены логарифмические оценки высоты.

---

### Профили и контакты

* **GitHub:** [@romanfan30](https://github.com/romanfan30)
* **Telegram:** [@Maestroairlines](https://t.me/Maestroairlines)
