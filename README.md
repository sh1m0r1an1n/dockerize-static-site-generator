# Docker Quick Reference

## Параметры сборки

- `ARG VERSION=main` - версия StaticJinjaPlus для сборки (тег или ветка)
- `ARG REPO=https://github.com/MrDave/StaticJinjaPlus.git` - репозиторий StaticJinjaPlus

## Быстрая сборка всех образов

<details>
<summary><strong>Для Linux/Mac:</strong></summary>

```bash
export DOCKER_USERNAME="имя_docker_пользователя"
export DOCKER_PATH="путь_до_dockerfile"

# Ubuntu-версии
docker build -f $DOCKER_PATH/Dockerfile.ubuntu --build-arg VERSION=0.1.0 -t $DOCKER_USERNAME/staticjinjaplus:0.1.0 $DOCKER_PATH
docker build -f $DOCKER_PATH/Dockerfile.ubuntu --build-arg VERSION=0.1.1 -t $DOCKER_USERNAME/staticjinjaplus:0.1.1 $DOCKER_PATH
docker build -f $DOCKER_PATH/Dockerfile.ubuntu -t $DOCKER_USERNAME/staticjinjaplus:develop $DOCKER_PATH
docker build -f $DOCKER_PATH/Dockerfile.ubuntu -t $DOCKER_USERNAME/staticjinjaplus:latest $DOCKER_PATH

# Slim-версии
docker build -f $DOCKER_PATH/Dockerfile.slim --build-arg VERSION=0.1.0 -t $DOCKER_USERNAME/staticjinjaplus:0.1.0-slim $DOCKER_PATH
docker build -f $DOCKER_PATH/Dockerfile.slim --build-arg VERSION=0.1.1 -t $DOCKER_USERNAME/staticjinjaplus:0.1.1-slim $DOCKER_PATH
docker build -f $DOCKER_PATH/Dockerfile.slim -t $DOCKER_USERNAME/staticjinjaplus:develop-slim $DOCKER_PATH
docker build -f $DOCKER_PATH/Dockerfile.slim -t $DOCKER_USERNAME/staticjinjaplus:slim $DOCKER_PATH
```

</details>

<details>
<summary><strong>Для Windows PowerShell:</strong></summary>

```powershell
$env:DOCKER_USERNAME="имя_docker_пользователя"
$env:DOCKER_PATH="путь_до_dockerfile"

# Ubuntu-версии
docker build -f $env:DOCKER_PATH\Dockerfile.ubuntu --build-arg VERSION=0.1.0 -t $env:DOCKER_USERNAME/staticjinjaplus:0.1.0 $env:DOCKER_PATH
docker build -f $env:DOCKER_PATH\Dockerfile.ubuntu --build-arg VERSION=0.1.1 -t $env:DOCKER_USERNAME/staticjinjaplus:0.1.1 $env:DOCKER_PATH
docker build -f $env:DOCKER_PATH\Dockerfile.ubuntu -t $env:DOCKER_USERNAME/staticjinjaplus:develop $env:DOCKER_PATH
docker build -f $env:DOCKER_PATH\Dockerfile.ubuntu -t $env:DOCKER_USERNAME/staticjinjaplus:latest $env:DOCKER_PATH

# Slim-версии
docker build -f $env:DOCKER_PATH\Dockerfile.slim --build-arg VERSION=0.1.0 -t $env:DOCKER_USERNAME/staticjinjaplus:0.1.0-slim $env:DOCKER_PATH
docker build -f $env:DOCKER_PATH\Dockerfile.slim --build-arg VERSION=0.1.1 -t $env:DOCKER_USERNAME/staticjinjaplus:0.1.1-slim $env:DOCKER_PATH
docker build -f $env:DOCKER_PATH\Dockerfile.slim -t $env:DOCKER_USERNAME/staticjinjaplus:develop-slim $env:DOCKER_PATH
docker build -f $env:DOCKER_PATH\Dockerfile.slim -t $env:DOCKER_USERNAME/staticjinjaplus:slim $env:DOCKER_PATH
```

</details>

<details>
<summary><strong>Для Windows Command Prompt:</strong></summary>

```cmd
set DOCKER_USERNAME=имя_docker_пользователя
set DOCKER_PATH=путь_до_dockerfile

# Ubuntu-версии
docker build -f %DOCKER_PATH%\Dockerfile.ubuntu --build-arg VERSION=0.1.0 -t %DOCKER_USERNAME%/staticjinjaplus:0.1.0 %DOCKER_PATH%
docker build -f %DOCKER_PATH%\Dockerfile.ubuntu --build-arg VERSION=0.1.1 -t %DOCKER_USERNAME%/staticjinjaplus:0.1.1 %DOCKER_PATH%
docker build -f %DOCKER_PATH%\Dockerfile.ubuntu -t %DOCKER_USERNAME%/staticjinjaplus:develop %DOCKER_PATH%
docker build -f %DOCKER_PATH%\Dockerfile.ubuntu -t %DOCKER_USERNAME%/staticjinjaplus:latest %DOCKER_PATH%

# Slim-версии
docker build -f %DOCKER_PATH%\Dockerfile.slim --build-arg VERSION=0.1.0 -t %DOCKER_USERNAME%/staticjinjaplus:0.1.0-slim %DOCKER_PATH%
docker build -f %DOCKER_PATH%\Dockerfile.slim --build-arg VERSION=0.1.1 -t %DOCKER_USERNAME%/staticjinjaplus:0.1.1-slim %DOCKER_PATH%
docker build -f %DOCKER_PATH%\Dockerfile.slim -t %DOCKER_USERNAME%/staticjinjaplus:develop-slim %DOCKER_PATH%
docker build -f %DOCKER_PATH%\Dockerfile.slim -t %DOCKER_USERNAME%/staticjinjaplus:slim %DOCKER_PATH%
```

</details>

## Публикация всех образов

<details>
<summary><strong>Для Linux/Mac:</strong></summary>

```bash
# Ubuntu-версии
docker push $DOCKER_USERNAME/staticjinjaplus:0.1.0
docker push $DOCKER_USERNAME/staticjinjaplus:0.1.1
docker push $DOCKER_USERNAME/staticjinjaplus:develop
docker push $DOCKER_USERNAME/staticjinjaplus:latest

# Slim-версии
docker push $DOCKER_USERNAME/staticjinjaplus:0.1.0-slim
docker push $DOCKER_USERNAME/staticjinjaplus:0.1.1-slim
docker push $DOCKER_USERNAME/staticjinjaplus:develop-slim
docker push $DOCKER_USERNAME/staticjinjaplus:slim
```

</details>

<details>
<summary><strong>Для Windows PowerShell:</strong></summary>

```powershell
# Ubuntu-версии
docker push $env:DOCKER_USERNAME/staticjinjaplus:0.1.0
docker push $env:DOCKER_USERNAME/staticjinjaplus:0.1.1
docker push $env:DOCKER_USERNAME/staticjinjaplus:develop
docker push $env:DOCKER_USERNAME/staticjinjaplus:latest

# Slim-версии
docker push $env:DOCKER_USERNAME/staticjinjaplus:0.1.0-slim
docker push $env:DOCKER_USERNAME/staticjinjaplus:0.1.1-slim
docker push $env:DOCKER_USERNAME/staticjinjaplus:develop-slim
docker push $env:DOCKER_USERNAME/staticjinjaplus:slim
```

</details>

<details>
<summary><strong>Для Windows Command Prompt:</strong></summary>

```cmd
# Ubuntu-версии
docker push %DOCKER_USERNAME%/staticjinjaplus:0.1.0
docker push %DOCKER_USERNAME%/staticjinjaplus:0.1.1
docker push %DOCKER_USERNAME%/staticjinjaplus:develop
docker push %DOCKER_USERNAME%/staticjinjaplus:latest

# Slim-версии
docker push %DOCKER_USERNAME%/staticjinjaplus:0.1.0-slim
docker push %DOCKER_USERNAME%/staticjinjaplus:0.1.1-slim
docker push %DOCKER_USERNAME%/staticjinjaplus:develop-slim
docker push %DOCKER_USERNAME%/staticjinjaplus:slim
```

</details>

## Проверка

```bash
# Список образов
docker images | grep staticjinjaplus

# Размеры образов
docker images --format "table {{.Repository}}:{{.Tag}}\t{{.Size}}" | grep staticjinjaplus

# Тест образа
docker run --rm -v $(pwd)/templates:/StaticJinjaPlus/templates $DOCKER_USERNAME/staticjinjaplus:latest
```

## Доступные теги и размеры

| Тег | Описание | Базовый образ | Содержимое | Размер |
|-----|----------|---------------|------------|--------|
| `latest` | Отдельная сборка | Ubuntu | develop | ~110.15 МБ |
| `slim` | Отдельная сборка | Python-slim | develop | ~78.4 МБ |
| `develop` | Последний коммит | Ubuntu | develop | ~110.15 МБ |
| `develop-slim` | Последний коммит | Python-slim | develop | ~78.4 МБ |
| `0.1.0` | Версия 0.1.0 | Ubuntu | 0.1.0 | ~111.15 МБ |
| `0.1.0-slim` | Версия 0.1.0 | Python-slim | 0.1.0 | ~79.56 МБ |
| `0.1.1` | Версия 0.1.1 | Ubuntu | 0.1.1 | ~110.16 МБ |
| `0.1.1-slim` | Версия 0.1.1 | Python-slim | 0.1.1 | ~78.41 МБ |