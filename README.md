# GYM FORCE

![CI/CD](https://github.com/VoidOnTheLeft/gym-force-cicd/actions/workflows/deploy.yml/badge.svg)

Учебный сайт спортивного зала с автоматическими проверками и автодеплоем через GitHub Actions.

Сайт: https://VoidOnTheLeft.github.io/gym-force-cicd/

## Как работает пайплайн

При каждом push в `main` запускается workflow `.github/workflows/deploy.yml`:

1. `lint` — проверка HTML (HTMLHint), CSS (Stylelint), синтаксиса JavaScript и наличия файлов, на которые ссылается страница.
2. `deploy` — публикация на GitHub Pages. Выполняется только если `lint` завершился успешно.
