cuayolo-API
===========

API-Rest de la plataforma de cuayolo.

## HTTP Verbs

 [HTTP/1.1](http://www.w3.org/Protocols/rfc2616/rfc2616-sec9.html) standard.

| HTTP METHOD | POST            | GET       | PUT         | DELETE |
| ----------- | --------------- | --------- | ----------- | ------ |
| CRUD OP     | CREATE          | READ      | UPDATE      | DELETE |
| /users       | Create new user | List user |  Data update | Delete all |
| /users/1234  | Error           | Show 1234   | If exists, update 1234; If not, error | Delete 1234 |

(Ejemplo de Web API Design)

## Error handling
```json
{
  "status" : 400,
  "developerMessage" : "Descriptiva, una descripción clara del problema. Proporcionar a los desarrolladores
    sugerencias sobre cómo resolver sus problemas aquí",
  "userMessage" : "Este es un mensaje que se puede pasar a los usuarios finales, si es necesario.",
  "errorCode" : "1234",
  "moreInfo" : "http://name.con/developer/path/to/help/for/1234"
}
```

- 200 - OK
- 400 - Bad Request
- 500 - Internal Server Error
