
# Dotfiles

## Варіант керування dotfiles (пункт 2.3)
Я обрав підхід **bare git repository** у `$HOME` (репозиторій зберігається в `~/.dotfiles`), а для керування використовую alias `config`.

Переваги цього підходу:
- конфігураційні файли залишаються у стандартних місцях 
- симлінки створються автоматично
- відновлення на новому профілі робиться швидко через `git clone --bare` + `config checkout`

Як використати на новому профілі

1) Клонувати bare-репозиторій
```bash
git clone --bare git@github.com:kernes52/dotfiles.git $HOME/.dotfiles

