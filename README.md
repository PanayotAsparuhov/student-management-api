# Spring Boot API за управление на студенти

## Описание
Това е Spring Boot REST API за управление на студенти, курсове, факултети и специалности. Осигурява крайни точки за CRUD операции върху тези обекти и използва PostgreSQL като база данни.

## Използвани технологии
- **Java 17+**
- **Spring Boot 3.1.4**
- **Spring Data JPA**
- **PostgreSQL**
- **Lombok** (за намаляване на шаблонния код)
- **MapStruct** (за мапване на DTO обекти)
- **Springdoc OpenAPI** (за документация на API с Swagger UI)
- **JUnit 5** (за тестване)

## Инсталиране и стартиране на проекта
### Предварителни изисквания
- Инсталирайте **Java 17** или по-нова версия
- Инсталирайте **Maven**
- Инсталирайте и конфигурирайте **PostgreSQL**

### Конфигуриране на базата данни
Редактирайте `application.properties` (или `application.yml`) в `src/main/resources/` и задайте настройките за PostgreSQL:
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/your_database
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```

### Компилиране и стартиране
```sh
mvn clean install
mvn spring-boot:run
```

### Достъп до документацията на API
След като приложението стартира, посетете:
[Swagger UI](http://localhost:8080/swagger-ui.html)

## Крайни точки на API
| Метод | Краен път | Описание |
|--------|---------------------------|-----------------------------|
| GET    | `/students` | Извличане на всички студенти |
| POST   | `/students` | Създаване на нов студент |
| GET    | `/students/{id}` | Извличане на студент по ID |
| PUT    | `/students/{id}` | Актуализиране на студент |
| DELETE | `/students/{id}` | Изтриване на студент |
| GET    | `/courses` | Извличане на всички курсове |
| ...    | Още крайни точки в Swagger |
