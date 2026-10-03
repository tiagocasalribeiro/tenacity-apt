# Tenacity – Repositório APT não oficial

Repositório Debian assinado para o **Tenacity**, compilado automaticamente a partir do [código-fonte oficial no Codeberg](https://codeberg.org/tenacityteam/tenacity) e atualizado diariamente.  
Instala o Tenacity com `apt` e recebe atualizações automáticas.

## Adicionar o repositório

Executa estes três comandos no terminal:

```bash
# 1. Importar a chave GPG do repositório
curl -fsSL https://tiagocasalribeiro.github.io/tenacity-apt/KEY.gpg \
  | sudo tee /etc/apt/trusted.gpg.d/tenacity.asc

# 2. Adicionar a fonte APT
echo "deb [arch=amd64 signed-by=/etc/apt/trusted.gpg.d/tenacity.asc] \
  https://tiagocasalribeiro.github.io/tenacity-apt stable main" \
  | sudo tee /etc/apt/sources.list.d/tenacity.list

# 3. Atualizar e instalar
sudo apt update
sudo apt install tenacity
