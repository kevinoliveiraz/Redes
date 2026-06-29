#  Tipos de Cabos de Rede (Ethernet)

## Conceito 
Cabos de rede são classificados por **categoria (Cat)**.  
Cada categoria define:
- **Frequência (MHz)** → capacidade de transmissão de sinal  
-  **Velocidade (Mbps/Gbps)** → taxa de dados suportada  
-  **Blindagem / interferência** → qualidade do sinal  

---

## Comparativo direto

| Categoria | Frequência | Velocidade Máxima | Uso típico |
|----------|-----------|------------------|-----------|
| **Cat5** | 100 MHz   | 100 Mbps         | Câmeras IP antigas |
| **Cat5e**| 100 MHz   | 1 Gbps           | Roteadores domésticos |
| **Cat6** | 250 MHz   | 1 Gbps (até 10 Gbps em curtas distâncias) | Switch / redes internas |
| **Cat6a**| 500 MHz   | 10 Gbps          | Servidores / empresas |
| **Cat7** | 600 MHz   | 10 Gbps          | Data centers |
| **Cat8** | 2000 MHz  | 25–40 Gbps       | Alta performance / datacenter avançado |

---

##  Explicação técnica 

### 1. Frequência (MHz)
- Representa quantas vezes o sinal pode oscilar por segundo
- Quanto maior → mais dados por segundo
- Analogia: estrada com mais faixas

---

### 2. Velocidade (Throughput)
- Limite prático de dados transmitidos
- Depende de:
  - cabo
  - hardware (placa de rede, switch)
  - interferência

---

### 3. Interferência (Ruído)
- Cabos melhores têm:
  - pares mais trançados
  - blindagem (STP vs UTP)
- Resultado: menos perda de pacote

---

## 🧪 Comparação prática

| Cenário | Melhor escolha |
|--------|--------------|
| Casa / internet comum | **Cat5e ou Cat6** |
| Streaming pesado / NAS | **Cat6** |
| Empresa / servidores | **Cat6a** |
| Data center | **Cat7 ou Cat8** |

---

## ⚠️ Observação
- **Cat7 e Cat8 quase não fazem sentido em casa**
- Limite real geralmente é o **roteador (1Gbps)**  
- Comprar Cat8 pra usar em internet de 300MB = desperdício

- <img width="1536" height="1024" alt="ChatGPT Image 8 de jun  de 2026, 21_02_16" src="https://github.com/user-attachments/assets/cb122c25-923b-4179-b727-ff88dc2fe17f" />


