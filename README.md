# SCANTHERA

**Scanner de segurança de rede local com dashboard web.**

Identifica todos os dispositivos da sua rede, analisa portas abertas, detecta vulnerabilidades conhecidas (CVEs), mapeia a topologia e monitora tráfego em tempo real — tudo em uma interface visual acessível pelo navegador.

![Dashboard](https://raw.githubusercontent.com/eulerazevedo/scanthera/main/preview.png)

---

## Download

Acesse a [página de releases](https://github.com/eulerazevedo/scanthera-releases/releases/latest) e baixe o executável para o seu sistema:

| Sistema | Arquivo |
|---|---|
| macOS | `scanthera-macos.zip` |
| Linux | `scanthera-linux.tar.gz` |
| Windows | `scanthera-windows.exe.zip` |

---

## Requisitos

O **nmap** precisa estar instalado no sistema:

```bash
# macOS
brew install nmap

# Ubuntu / Debian
sudo apt install nmap

# Fedora
sudo dnf install nmap
```

Windows: baixe em [nmap.org/download.html](https://nmap.org/download.html)

---

## Como usar

### macOS / Linux

```bash
# Extraia o arquivo e execute com privilégios de root
sudo ./scanthera
```

> **macOS — aviso de segurança:** Na primeira execução o macOS pode bloquear o app por não ter assinatura Apple. Para liberar, execute no terminal:
> ```bash
> sudo xattr -rd com.apple.quarantine ./scanthera-macos
> sudo ./scanthera-macos
> ```
> Ou clique com o botão direito no arquivo → segure **Option (⌥)** → clique **"Abrir"** → **"Abrir"**.

### Windows

Extraia o `.zip`, clique com o botão direito em `scanthera-windows.exe` → **Executar como administrador**.

> Privilégios de administrador/root são necessários para ARP scan, OS fingerprinting e captura de pacotes.

---

## Funcionalidades

- **Descoberta de rede** — detecta dispositivos via ARP + ping
- **Scan de portas** — identifica serviços ativos e portas perigosas expostas
- **Detecção de OS** — fingerprinting do sistema operacional de cada dispositivo
- **CVEs** — consulta automática na base NVD para vulnerabilidades conhecidas
- **Topologia** — mapa visual da rede com relações entre dispositivos
- **Captura de pacotes** — monitoramento de tráfego em tempo real com alerta para tráfego sem criptografia
- **WiFi** — análise de redes sem fio disponíveis e segurança
- **Relatórios** — exportação em PDF e HTML
- **Score de risco** — pontuação automática de risco por dispositivo

---

## Após executar

O dashboard abre automaticamente no navegador em `http://localhost:7777`.

---

Desenvolvido por [Euler Azevedo](https://github.com/eulerazevedo)
