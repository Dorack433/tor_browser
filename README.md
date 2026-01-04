# Tor Browser — Instalador Automático

Este script automatiza a instalação do **Tor Browser** no Linux a partir do pacote oficial do Tor Project.

Ele realiza automaticamente:

1. Download do Tor Browser
2. Extração do arquivo
3. Movimentação para `/opt/tor-browser`
4. Registro do aplicativo no sistema usando `--register-app`

Depois disso, o Tor Browser passa a aparecer no menu de aplicativos.

---

## 📥 Download oficial utilizado

```
https://www.torproject.org/dist/torbrowser/15.0.3/tor-browser-linux-x86_64-15.0.3.tar.xz
```

---

## ✅ Requisitos

* Sistema baseado em Linux (Ex.: Debian, Ubuntu, Mint, etc.)
* Acesso root (ou `sudo`)
* `wget` instalado

Se não tiver o `wget`, instale com:

```
sudo apt install wget -y
```

---

## ▶️ Como usar o script

1. Salve o script em um arquivo, por exemplo:

```
instalar-tor.sh
```

2. Dê permissão de execução:

```
chmod +x instalar-tor.sh
```

3. Execute como root:

```
sudo ./instalar-tor.sh
```

---

## 📂 Caminho de instalação

O Tor Browser será instalado em:

```
/opt/tor-browser
```

---

## 🎯 Registro do aplicativo

O script registra o Tor Browser no menu do sistema:

```
start-tor-browser.desktop --register-app
```

Após isso, você pode abrir o Tor Browser:

* Pelo menu de aplicativos
* Ou via terminal:

```
/opt/tor-browser/start-tor-browser.desktop
```

---

## ♻️ Atualizações

O Tor Browser possui atualizador interno.
Basta abrir o navegador e usar o atualizador integrado quando aparecer.

---

## ❌ Desinstalação

Para remover:

```
sudo rm -rf /opt/tor-browser
```

E remova atalhos registrados:

```
sudo update-desktop-database
```

---

## ⚠️ Observações importantes

* Baixe sempre do site oficial do Tor Project.
* Evite instalar versões modificadas de terceiros.
* Execute o script apenas se confiar nele e entender o que ele faz.

---
