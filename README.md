# Лабораторная работа №28. Веб-сервер на C#: список любимых игр с полным управлением

Веб-сервер на ASP.NET Core для управления списком игр. Поддерживает полное CRUD управление: получение списка игр, добавление новых, обновление и удаление.

## Инструкция по запуску

```bash
cd GamesApi && dotnet run
```
---

## Таблица маршруто
| Метод | Маршрут | Описание | Статус |
| :--- | :--- | :--- | :--- |
| GET | `/api/games` | Получить все игры | 200 |
| GET | `/api/games/{id}` | Получить игру по id | 200 / 404 |
| POST | `/api/games` | Добавить игру | 201 |
| DELETE | `/api/games/{id}` | Удалить игру | 204 / 404 |
| PUT | `/api/games/{id}` | Обновить игру | 200 / 404 |
---
## Примеры curl-команд
Получить все игры

```bash
curl http://localhost:5000/api/games
```
## Получить игру по id
```bash
curl http://localhost:5000/api/games/1
```
## Добавить новую игру
```bash
curl -X POST http://localhost:5000/api/games \
  -H "Content-Type: application/json" \
  -d "{\"title\":\"Stardew Valley\",\"genre\":\"Simulation\",\"releaseYear\":2016}"
  ```
  ## Обновить игру
  ```bash
 curl -X PUT http://localhost:5000/api/games/2 \
  -H "Content-Type: application/json" \
  -d "{\"title\":\"The Witcher 3\",\"genre\":\"RPG\",\"releaseYear\":2015}"
  ```
  ## Удалить игру
   ```bash
   curl -X DELETE http://localhost:5000/api/games/1
   ```
## Получить статусный код
```bash
curl -i http://localhost:5000/api/games
```
## Технологии
- ASP.NET Core
- C#
- Controllers API
- In-memory storage
## Автор
Текутова В.Д. ИСП-231
10.04.26