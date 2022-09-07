# Spring Boot CRUD - almost tutorial
Linux / IntelliJ IDEA / Spring Boot / Gradlev / Postgress / Crud

This is an example Spring Boot application that uses Java, and communicates with an postgres database

| Technical information                     |
| :---------------------------------------- |
| [Preconditions](#Preconditions)           |
| [Dependencies](#Dependencies)             |

### Versions:
| Tags               | Changes steps                                                      |
| :----------------- | :----------------------------------------------------------------- |
| [biosquare-v0.0](https://github.com/VoltG3/spring_boot_biosquare//releases/tag/biosquare-v3.0) | [empty template](#chapter-biosquare-v00)                                  |
| [biosquare-v1.0](https://github.com/VoltG3/spring_boot_biosquare/releases/tag/biosquare-v3.0) | [isAppOnloaded controller](#chapter-biosquare-v10) 
| [biosquare-v2.0](https://github.com/VoltG3/spring_boot_biosquare/releases/tag/biosquare-v3.0) | [liquibase migration](#chapter-biosquare-v20) |
| [biosquare-v3.0](https://github.com/VoltG3/spring_boot_biosquare/releases/tag/biosquare-v3.0) | [crud](#chapter-biosquare-v30) |

### CHAPTER biosquare-v0.0
- [ empty template ] - Project configuration example based on intelliJ IDEA

<table>
  <tr>
    <td><img src="https://github.com/VoltG3/doc/blob/master/readme_img/spring_boot_biosquare/img001.png" width="500" alt="img"></td>
    <td><img src="https://github.com/VoltG3/doc/blob/master/readme_img/spring_boot_biosquare/img002.png" width="500" alt="img"></td>
  <tr>
 </table>

### CHAPTER biosquare-v1.0
- [ isAppOnloaded controller ] - First Controller
 
To get response type in browser
```
http://localhost:8080/isAppOnloaded
```
<table>
  <tr>
    <td><img src="https://github.com/VoltG3/doc/blob/master/readme_img/spring_boot_biosquare/img101.png" width="350" alt="img"></td>
  <tr>
 </table>
   
### CHAPTER biosquare-v2.0
- [ liquibase migration ] - Migrate sql scripts
   
<table>
  <tr>
    <td><img src="https://github.com/VoltG3/doc/blob/master/readme_img/spring_boot_biosquare/img201.png" width="1000" alt="img"></td>
  <tr>
 </table>
 
 > if this error message, then create directories separately, first "db", then "changelog"
 
### CHAPTER biosquare-v3.0
- [ crud ] - operations
   
<table>
  <tr>
    <td><img src="https://github.com/VoltG3/doc/blob/master/readme_img/spring_boot_biosquare/img301.png" width="700" alt="img"></td>
  <tr>
 </table>
 
#### Operations examples
##### GET all RECORDS
Request:
```
GET http://localhost:8080/biosquares
```
Response:
```JSON
[
    {
        "id": 1,
        "landcode": "ae",
        "landname": "United Arab Emirates  ",
        "region": "africa",
        "population": 9890402,
        "landarea": 83.6,
        "landmap": "https://danoss.no/BioSquare/maps/ae.svg"
    },
```
##### GET RECORD by ID
Request:
```
GET http://localhost:8080/biosquares/145
```
Response:
```JSON
{
    "id": 145,
    "landcode": "is",
    "landname": "Iceland  ",
    "region": "europa",
    "population": 341,
    "landarea": 100.25,
    "landmap": "https://danoss.no/BioSquare/maps/is.svg"
}
```
##### CREATE new RECORD
Request:
```
POST http://localhost:8080/biosquares
```
Response:
```JSON
{
    "landcode": "zz",
    "landname": "unknown  ",
    "region": "none",
    "population": 0,
    "landarea": 0,
    "landmap": "none"
}
```
##### DELETE RECORD
Reques:
```
DELETE http://localhost:8080/biosquares/246
```
Response:
```JSON
{
    "deleted": true
}
```
##### UPDATE RECORD under construction
 
## Preconditions
- Linux https://ubuntu.com/
- IntelliJ IDEA https://www.jetbrains.com/idea/
- Java https://sdkman.io/
- Docker https://docs.docker.com/engine/install/ubuntu/
- Postman https://www.postman.com/downloads/
- DBeaver https://dbeaver.io/

## Dependencies
Use Spring initializr https://start.spring.io/ for more info
- spring-boot-starter-web
- spring-boot-starter-data-jpa
- org.liquibase:liquibase-core
- org.postgresql:postgresql
- org.projectlombok:lombok
- org.springframework.boot:spring-boot-devtools




