# guia-linux-essencial
Um guia de consulta rápida com os comandos essenciais do Linux
# Guia Essencial de Comandos Linux 🐧

Bem-vindo! Este repositório é um guia com os comandos essenciais do Linux, pensado para estudantes como introdução e material suplementar no curso Processamento de Dados de Sequenciamento de Nova Geração Gerados por Bibliotecas de Target Sequencing Capture.

O objetivo é fornecer explicações claras e exemplos práticos que possam ser úteis no dia a dia.

## Índice

1.  [Navegação e Exploração do Sistema](#1-navegação-e-exploração-do-sistema)
2.  [Manipulação de Arquivos e Diretórios](#2-manipulação-de-arquivos-e-diretórios)
3.  [Visualização e Inspeção de Conteúdo](#3-visualização-e-inspeção-de-conteúdo)
4.  [Busca e Edição](#4-busca-e-edição)
5.  [Gerenciamento do Sistema e Ajuda](#5-gerenciamento-do-sistema-e-ajuda)

---

### **1. Navegação e Exploração do Sistema**

Comandos para se localizar e mover dentro da estrutura de diretórios.

#### `pwd`
* **Função:** (Print Working Directory) Mostra o caminho completo do diretório atual.
* **Exemplo:**
    ```bash
    # Descubra em qual pasta você está agora
    pwd
    # Saída esperada: /home/seu_usuario/Documentos
    ```

#### `ls`
* **Função:** (List) Lista o conteúdo de um diretório.
* **Exemplos:**
    ```bash
    # Listar o conteúdo da pasta atual de forma simples
    ls

    # Listar com detalhes (tamanhos em K, M, G)
    ls -lh

    # Listar incluindo todos os arquivos ocultos
    ls -a
    ```

#### `cd`
* **Função:** (Change Directory) Muda de um diretório para outro.
* **Exemplos:**
    ```bash
    # Entrar na pasta 'Documentos'
    cd Documentos

    # Voltar para o diretório anterior (pai)
    cd ..

    # Voltar diretamente para sua pasta pessoal (home) de qualquer lugar
    cd ~
    ```

#### `clear`
* **Função:** Limpa a tela do terminal.
* **Exemplo:**
    ```bash
    # A tela está cheia de comandos? Limpe-a.
    clear
    # Atalho comum: Ctrl + L
    ```

---

### **2. Manipulação de Arquivos e Diretórios**

Comandos para criar, copiar, mover e apagar.

#### `mkdir`
* **Função:** (Make Directory) Cria um novo diretório.
* **Exemplo:**
    ```bash
    # Criar uma pasta para o seu novo projeto
    mkdir meu_projeto
    ```

#### `cp`
* **Função:** (Copy) Copia arquivos ou diretórios.
* **Exemplos:**
    ```bash
    # Copiar um arquivo para outro local
    cp arquivo.txt /home/seu_usuario/Documentos/

    # Copiar uma pasta inteira (requer a opção -r de recursivo)
    cp -r meu_projeto /backup/
    ```

#### `mv`
* **Função:** (Move) Move ou renomeia arquivos e diretórios.
* **Exemplos:**
    ```bash
    # Renomear um arquivo
    mv relatorio_velho.txt relatorio_novo.txt

    # Mover um arquivo para outra pasta
    mv relatorio_novo.txt ./arquivos_finais/
    ```

#### `rm`
* **Função:** (Remove) Apaga arquivos ou diretórios. **CUIDADO: Não há lixeira!**
* **Exemplos:**
    ```bash
    # Apagar um arquivo
    rm arquivo_temporario.txt

    # Apagar uma pasta vazia
    rmdir pasta_vazia

    # Apagar uma pasta e todo o seu conteúdo (use com extrema cautela!)
    rm -r pasta_para_deletar
    ```
---

### **3. Visualização e Inspeção de Conteúdo**
Comandos para ler e analisar o conteúdo de arquivos.

#### `cat`
* **Função:** (Concatenate) Exibe o conteúdo de um ou mais arquivos.
* **Exemplo:**
    ```bash
    # Ler o conteúdo de um arquivo de configuração
    cat /etc/os-release
    ```

#### `less`
* **Função:** Visualiza o conteúdo de arquivos grandes de forma navegável.
* **Exemplo:**
    ```bash
    # Abrir um arquivo de log grande para inspecionar
    less /var/log/syslog
    # Aperte 'q' para sair.
    ```

#### `head` / `tail`
* **Função:** `head` mostra o início de um arquivo; `tail` mostra o final.
* **Exemplos:**
    ```bash
    # Ver as 5 primeiras linhas de um arquivo
    head -n 5 meu_arquivo.csv

    # Ver as 10 últimas linhas de um log e continuar vendo em tempo real
    tail -n 10 -f log_do_servidor.log
    ```

#### `wc`
* **Função:** (Word Count) Conta linhas, palavras e caracteres.
* **Exemplo:**
    ```bash
    # Contar quantas linhas (sequências) existem em um arquivo FASTA
    wc -l meu_arquivo.fasta
    ```
---

### **4. Busca e Edição**

#### `grep`
* **Função:** Busca por padrões de texto dentro de arquivos.
* **Exemplos:**
    ```bash
    # Encontrar todas as linhas que contêm a palavra "ERROR" em um log
    grep "ERROR" /var/log/syslog

    # Procurar por uma sequência de DNA em um arquivo, ignorando maiúsculas/minúsculas
    grep -i "ATGCGTG" sequencias.fasta
    ```

#### `nano`
* **Função:** Um editor de texto simples e intuitivo para o terminal.
* **Exemplo:**
    ```bash
    # Abrir um script para edição
    nano meu_script.sh
    # Use Ctrl+O para salvar e Ctrl+X para sair.
    ```
---

### **5. Gerenciamento do Sistema e Ajuda**

#### `man`
* **Função:** (Manual) Exibe a página de manual de qualquer comando.
* **Exemplo:**
    ```bash
    # Quer saber todas as opções do comando 'ls'?
    man ls
    # Aperte 'q' para sair.
    ```

#### `echo`
* **Função:** Imprime um texto na tela. Útil em scripts.
* **Exemplo:**
    ```bash
    # Imprimir uma mensagem
    echo "O script comecou a rodar..."
    ```

#### `sudo apt update / install`
* **Função:** Gerenciador de pacotes para sistemas baseados em Debian/Ubuntu.
* **Exemplos:**
    ```bash
    # Primeiro, sempre atualize a lista de pacotes disponíveis
    sudo apt update

    # Depois, instale o programa desejado (ex: htop)
    sudo apt install htop
    ```

---

## Como Contribuir

Viu algum erro ou tem um exemplo melhor? Sinta-se à vontade para abrir uma *Issue* ou enviar um *Pull Request*!

---

## Para Ir Além: Aprofunde Seus Conhecimentos

Aprender a linha de comando é uma jornada contínua. Os comandos neste guia são a base, mas há um universo de possibilidades. Aqui estão alguns recursos fantásticos e gratuitos para você continuar seus estudos:

### Livros e Guias Completos

* [**The Linux Command Line**](https://linuxcommand.org/tlcl.php) - *(em Inglês)* Um livro bem completo e didático para aprender do zero. O PDF é gratuito.
* [**Guia Foca Linux**](https://www.guiafoca.org/) - *(em Português)* Um guia da comunidade brasileira. Cobre desde o nível iniciante até o avançado.

### Tutoriais Interativos (Aprender Fazendo)

* [**OverTheWire: Bandit**](https://overthewire.org/wargames/bandit/) - *(em Inglês)* Aprenda Linux de uma forma gamificada! O Bandit é um jogo onde você precisa usar comandos para resolver desafios e "hackear" o próximo nível.
* [**Linux Journey**](https://linuxjourney.com/) - *(em Inglês)* Um site com lições curtas e diretas, com um terminal interativo no navegador para você praticar cada conceito logo após aprendê-lo.

### Referência Rápida e Comunidades

* [**tldr pages**](https://tldr.sh/) - *("Too Long; Didn't Read")* Uma versão simplificada das páginas `man`. Mostra os 3 ou 4 exemplos mais comuns de cada comando.
* **Comunidades Online:**
       * **Reddit:** Subreddits como `r/linux`, `r/linuxquestions` e `r/linux4noobs` são ótimos para discussões e para pedir ajuda.

---

## Licença

Este projeto está sob a [MIT License](LICENSE).
