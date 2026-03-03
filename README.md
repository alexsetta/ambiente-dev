# Ambiente de Desenvolvimento

## Terminal

- [Windows Terminal](https://www.microsoft.com/pt-br/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab) - Terminal moderno e personalizável para Windows.
- [Zsh +  Oh My Zsh](https://ohmyz.sh/) - Zsh é um shell poderoso e personalizável, e Oh My Zsh é um framework para gerenciar a configuração do Zsh.


### Em caso de lentidão do Zsh:
- zcompile ~/.zshrc && zcompile ~/ams.sh
- time ZSH_DEBUGLOG=1 zsh -i -c exit
    (precisa ser executado em menos de 0.2s, caso contrário, o problema pode estar relacionado a plugins ou configurações específicas do Zsh)