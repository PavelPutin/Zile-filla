# Zile-filla
Клиент-серверное приложение, позволяющее осуществлять навигацию по файловой системе сервера.

Концепт веб-интерфейса: [Figma](https://www.figma.com/design/jl2lotfkwN4oi9q5s4sYB1/Zile-Filla?node-id=0-1&t=YPtiTHtGzySce1K8-1)

## Инструкция по запуску (Docker compose)

1. Создайте файл .env и определите переменные окружения, указанные в .env.origin;
2. В файле compose.yaml volume, который будет связывать корень поддерва с публикуемыми файлами, например

```yaml
services:
  backend:
    ...
    volumes:
      - "C:\\custom-root:${EXPOSE_SUBTREE_ROOT}"
    ...
```
3. Запустите `docker compose up -d` из папки проекта;
4. Откроете приложение, перейдя по ссылке http://localhost:3000
