# ambiente-dev

Guia para configurar o ambiente de desenvolvimento local.

---

## Pré-requisitos

Antes de começar, certifique-se de ter instalado em sua máquina:

- [Git](https://git-scm.com/) (versão 2.x ou superior)
- [Node.js](https://nodejs.org/) (versão 18.x ou superior) — inclui o `npm`
- Um editor de código, como o [Visual Studio Code](https://code.visualstudio.com/)

---

## 1. Instalação das ferramentas

### Git

**Linux (Debian/Ubuntu):**
```bash
sudo apt update
sudo apt install git
```

**macOS (com Homebrew):**
```bash
brew install git
```

**Windows:**  
Baixe e execute o instalador em https://git-scm.com/download/win

Verifique a instalação:
```bash
git --version
```

---

### Node.js

Recomendamos usar o **nvm** (Node Version Manager) para facilitar o gerenciamento de versões.

**Linux / macOS:**
```bash
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.7/install.sh | bash
# Reinicie o terminal e instale a versão LTS do Node.js:
nvm install --lts
nvm use --lts
```

**Windows:**  
Use o [nvm-windows](https://github.com/coreybutler/nvm-windows) ou baixe o instalador diretamente em https://nodejs.org/

Verifique a instalação:
```bash
node --version
npm --version
```

---

## 2. Configuração inicial do Git

Configure seu nome e e-mail globalmente (substituindo pelos seus dados):

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

Configure o editor padrão (opcional, exemplo com VS Code):

```bash
git config --global core.editor "code --wait"
```

---

## 3. Clonando o repositório

```bash
git clone https://github.com/alexsetta/ambiente-dev.git
cd ambiente-dev
```

---

## 4. Instalando as dependências

Após clonar o repositório, instale as dependências do projeto:

```bash
npm install
```

---

## 5. Variáveis de ambiente

Copie o arquivo de exemplo e ajuste os valores conforme necessário:

```bash
cp .env.example .env
```

Abra o arquivo `.env` e preencha as variáveis de acordo com o seu ambiente local. Nunca envie o arquivo `.env` para o repositório — ele já está listado no `.gitignore`.

---

## 6. Executando o projeto

Para iniciar o servidor de desenvolvimento:

```bash
npm run dev
```

Acesse a aplicação em [http://localhost:3000](http://localhost:3000).

---

## 7. Executando os testes

Para rodar a suíte de testes:

```bash
npm test
```

---

## 8. Fluxo de trabalho com Git

Siga o fluxo abaixo para contribuir com o projeto:

1. **Crie uma branch** a partir da `main`:
   ```bash
   git checkout -b feature/minha-funcionalidade
   ```

2. **Faça suas alterações** e realize commits descritivos:
   ```bash
   git add .
   git commit -m "feat: adiciona nova funcionalidade"
   ```

3. **Envie a branch** para o repositório remoto:
   ```bash
   git push origin feature/minha-funcionalidade
   ```

4. **Abra um Pull Request** no GitHub e aguarde a revisão.

---

## 9. Extensões recomendadas para o VS Code

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier – Code formatter](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
- [EditorConfig for VS Code](https://marketplace.visualstudio.com/items?itemName=EditorConfig.EditorConfig)

---

## Problemas comuns

| Problema | Solução |
|---|---|
| `npm install` falha com erro de permissão | Evite usar `sudo`; configure o npm para instalar globalmente sem permissões elevadas ([guia](https://docs.npmjs.com/resolving-eacces-permissions-errors-when-installing-packages-globally)) |
| Porta 3000 já em uso | Altere a variável `PORT` no arquivo `.env` para outra porta disponível |
| Versão do Node.js incompatível | Use o `nvm` para instalar a versão correta especificada no campo `engines` do `package.json` |

---

## Contribuindo

Contribuições são bem-vindas! Abra um Pull Request com uma descrição clara das alterações realizadas.

---

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
