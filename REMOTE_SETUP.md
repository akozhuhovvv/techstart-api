# Remote Repository Setup

## Current Remotes
[Вставьте вывод git remote -v]
backup	git@github.com:akozhuhovvv/techstart-api-backup.git (fetch)
backup	git@github.com:akozhuhovvv/techstart-api-backup.git (push)
origin	git@github.com:akozhuhovvv/techstart-api.git (fetch)
origin	git@github.com:akozhuhovvv/techstart-api.git (push)
origin	git@github.com:akozhuhovvv/techstart-api-backup.git (push)

## Tracking Branches
[Вставьте вывод git branch -vv]
  develop 88a841a [origin/develop] Bump version to 1.1.0-dev
* main    88f0530 Resolve merge conflict


## Fork Workflow Summary
- Original repository: https://github.com/akozhuhovvv/techstart-api
- Fork repository: https://github.com/akozhuhovvv/techstart-api-fork
- Upstream configuration: git remote add upstream https://github.com/akozhuhovvv/techstart-api.git

## Backup Strategy
- Primary remote: origin
- Backup remote: backup
- Sync command: [команда для синхронизации]
git push origin main  # пушит в origin и backup одновременно, если настроено:
git remote set-url --add --push origin git@github.com:akozhuhovvv/techstart-api.git
git remote set-url --add --push origin git@github.com:akozhuhovvv/techstart-api-backup.git

## Lessons Learned
Работа с удалёнными репозиториями помогает синхронизировать изменения между членами команды
и обеспечивает резервное копирование. Fork workflow удобно использовать для работы с чужими проектами,
а настройка upstream даёт гибкость для получения и интеграции изменений из оригинала.
Возможность отправлять код сразу в два удалённых репозитория повышает надёжность хранения кода.

