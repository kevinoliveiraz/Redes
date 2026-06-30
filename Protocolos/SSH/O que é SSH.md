# SSH (Secure Shell)

## O que é o SSH?

**SSH (Secure Shell)** é um protocolo de rede que permite acessar e controlar outro computador de forma **remota e segura** através de uma rede local ou da internet.

Ele cria uma conexão criptografada entre o dispositivo cliente e o servidor, garantindo que todas as informações transmitidas permaneçam protegidas contra interceptação.

Uma forma simples de entender é imaginar o SSH como um **túnel seguro e criptografado** entre dois computadores.

---

# Como o SSH funciona?

O funcionamento do SSH pode ser resumido em três etapas principais.

## 1. Acesso via Terminal

O SSH fornece acesso remoto através de um **terminal (linha de comando)**.

Após a conexão, é possível:

- Executar comandos
- Instalar programas
- Editar arquivos
- Reiniciar serviços
- Gerenciar usuários
- Administrar todo o sistema operacional

Diferente de programas como AnyDesk ou RustDesk, o SSH **não possui interface gráfica** por padrão.

---

## 2. Criptografia de ponta a ponta

Toda a comunicação entre o cliente e o servidor é criptografada.

Isso significa que:

- Os comandos enviados ficam protegidos.
- As respostas do servidor também são protegidas.
- Mesmo que alguém intercepte os pacotes da rede, verá apenas dados criptografados.

Essa criptografia é um dos principais motivos pelos quais o SSH é amplamente utilizado para administração de servidores.

---

## 3. Autenticação

Antes de permitir o acesso, o servidor verifica a identidade do usuário.

Existem duas formas principais de autenticação:

### Senha

O método mais simples.

O usuário informa seu nome de usuário e senha para acessar o servidor.

### Chaves SSH

Método recomendado.

Funciona utilizando um par de chaves criptográficas:

- Chave pública
- Chave privada

A chave pública fica armazenada no servidor, enquanto a chave privada permanece apenas no dispositivo do usuário.

Esse método é muito mais seguro do que utilizar apenas senhas.

---

# Principais usos do SSH

O SSH é utilizado diariamente por administradores de sistemas, desenvolvedores e profissionais de infraestrutura.

Os usos mais comuns incluem:

## Administração de servidores

Permite administrar servidores Linux remotamente.

Exemplos:

- Atualizar o sistema
- Instalar programas
- Configurar serviços
- Reiniciar servidores
- Monitorar recursos

---

## Transferência segura de arquivos

Além do terminal, o SSH também permite enviar e receber arquivos utilizando protocolos como:

- `scp`
- `sftp`

Esses protocolos utilizam a mesma conexão criptografada do SSH.

---

## Automação

É possível executar comandos automaticamente em computadores remotos.

Isso é muito utilizado para:

- Backups automáticos
- Atualizações
- Deploy de aplicações
- Scripts de manutenção

---

## Gerenciamento de dispositivos

Também é muito utilizado para acessar:

- Raspberry Pi
- Servidores domésticos (Homelab)
- NAS
- Máquinas virtuais
- Containers Docker
- Equipamentos de rede

---

# Exemplo de conexão

O comando básico para acessar um servidor via SSH é:

```bash
ssh usuario@endereco_do_servidor
```

Exemplo:

```bash
ssh kevin@192.168.0.50
```

ou

```bash
ssh root@meuservidor.com
```

Após a autenticação, o terminal remoto será aberto.

---

# Porta padrão

Por padrão, o SSH utiliza a porta:

```
22
```

É possível alterar essa porta no servidor para reduzir tentativas automáticas de invasão.

Exemplo utilizando outra porta:

```bash
ssh usuario@servidor -p 2222
```

---

# Vantagens do SSH

- Comunicação totalmente criptografada
- Baixo consumo de banda
- Alta velocidade
- Administração remota segura
- Funciona em praticamente qualquer sistema operacional
- Pode ser utilizado pela internet ou rede local

