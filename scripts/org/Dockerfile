# Берем официальный Pandoc
FROM pandoc/core:latest

# Добавляем curl, чтобы скачать Task
RUN apk add --no-cache curl && \
    sh -c "$(curl --location https://taskfile.dev/install.sh)" -- -d -b /usr/local/bin && \
    apk del curl

# Рабочая директория
WORKDIR /work

# По умолчанию запускаем task
ENTRYPOINT ["task"]