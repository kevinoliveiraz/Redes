# Traceroute — Entendendo o Caminho da Internet

O comando `traceroute` (Linux) ou `tracert` (Windows) permite visualizar o caminho que os pacotes percorrem até chegar a um destino na internet.

Ele mostra cada roteador (hop/salto) entre o seu computador e o servidor de destino.

# Instalação (Linux)

Algumas distribuições Linux não possuem o comando `traceroute` instalado por padrão.

Caso receba a mensagem:

```text
Comando 'traceroute' não encontrado
```

Instale com:

Debian, Ubuntu, Linux Mint e derivados:

```bash
sudo apt update
sudo apt install traceroute
```

Fedora:

```bash
sudo dnf install traceroute
```

Arch Linux:

```bash
sudo pacman -S traceroute
```

Após a instalação, verifique se o comando está disponível:

```bash
traceroute --version
```


# Instalação Android (Termux)

Instalação:

```bash
pkg update
pkg install traceroute
```


---

# Como Funciona

Quando você acessa um site, os dados não vão diretamente do seu computador para o servidor.

Eles passam por diversos equipamentos da rede.

Fluxo simplificado:

```text
Seu PC
   ↓
Seu Roteador
   ↓
Provedor de Internet
   ↓
Backbones da Internet
   ↓
Rede da Microsoft
   ↓
www.msn.com.br
```

O traceroute mostra cada uma dessas etapas.

---

# Exemplo de Saída

```text
1  192.168.0.1        1 ms
2  10.0.0.1           5 ms
3  177.x.x.x          8 ms
4  200.x.x.x         15 ms
5  msn.com.br        20 ms
```

---

# Entendendo Cada Linha

### Salto 1

```text
192.168.0.1
```

Normalmente é o seu roteador doméstico.

---

### Saltos Intermediários

```text
10.0.0.1
177.x.x.x
200.x.x.x
```

São roteadores da operadora ou da infraestrutura da internet.

Eles encaminham os pacotes até o destino.

---

### Destino Final

```text
msn.com.br
```

É o servidor que respondeu ao teste.

---

# O que Significa "ms"?

Exemplo:

```text
20 ms
```

"ms" significa milissegundos.

É o tempo que o pacote levou para chegar até aquele ponto e voltar.

Quanto menor o valor, melhor.

Exemplo:

| Latência | Situação |
|-----------|----------|
| 1–20 ms | Excelente |
| 20–50 ms | Muito boa |
| 50–100 ms | Boa |
| 100–200 ms | Perceptível |
| Acima de 200 ms | Alta latência |

---

# O que Significa um Hop?

Hop significa "salto".

Cada hop representa um equipamento de rede que encaminhou seu pacote.

Exemplo:

```text
Hop 1 → Seu roteador
Hop 2 → Operadora
Hop 3 → Backbone
Hop 4 → Rede da Microsoft
Hop 5 → Servidor final
```

---

# Quando Aparece "* * *"

Exemplo:

```text
7  * * *
```

Isso normalmente significa que aquele equipamento:

- Bloqueia respostas do traceroute;
- Está configurado para não responder;
- Possui filtragem de segurança.

Nem sempre indica problema.

---

# Para Que Serve?

O traceroute é usado para:

- Diagnóstico de rede;
- Encontrar pontos de lentidão;
- Verificar rotas da internet;
- Identificar falhas entre provedores;
- Analisar perda de conectividade.

---

# Exemplos Úteis

Google:

```bash
traceroute google.com
```

GitHub:

```bash
traceroute github.com
```

Cloudflare:

```bash
traceroute 1.1.1.1
```

DNS Google:

```bash
traceroute 8.8.8.8
```

---

# Teste Linux,Windows e Android

Linux:

```bash
traceroute google.com
```

Windows:

```cmd
tracert google.com
```

Android:
```termux
traceroute google.com
```
Ambos possuem a mesma finalidade.

---

# Resumo

O traceroute permite visualizar o caminho que os dados percorrem pela internet.

Ele mostra:

- Cada roteador atravessado;
- O tempo de resposta de cada salto;
- Possíveis pontos de falha ou lentidão.

É uma das ferramentas mais utilizadas por profissionais de redes e suporte para diagnosticar problemas de conectividade.
