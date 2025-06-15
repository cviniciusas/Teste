# ArkSH - Gerenciador de Usuários e Conexões

O **ArkSH** é um gerenciador de usuários e conexões para servidores Linux, desenvolvido para ser **leve**, **eficiente** e **totalmente independente de outros sistemas ou bancos de dados externos**.

---

## 📌 Características Principais

- ✅ **Gerenciamento direto nos arquivos nativos do sistema**  
Sem uso de bancos de dados como `usuarios.db` ou estruturas artificiais.

- ✅ **Compatível com outros gerenciadores**  
Pode coexistir com sistemas como **SSHPLUS**, **SSHorizon**, entre outros, sem conflitos.

- ✅ **Limite de Conexões Inteligente**  
Por padrão, todos os usuários reais (UID > 1000) têm **limite de 1 conexão simultânea**.  
Ao exceder o limite, **a conexão mais antiga (PID mais antigo) é encerrada automaticamente**, evitando sessões fantasma.

- ✅ **Gerenciamento de Protocolos**  
Compatível com **SSH**, **Dropbear**, **OpenVPN**, e outros, trabalhando **diretamente nos arquivos de configuração nativos de cada serviço**, independente da forma de instalação.

- ✅ **Leitura de usuários somente nos arquivos reais do sistema**  
Usuários criados apenas em bancos locais (ex: `usuarios.db`) **não serão reconhecidos**.  
Somente **usuários reais presentes no sistema** aparecem no ArkSH.

---

## ⚙️ Menu de Configurações

O ArkSH possui um **painel interno de configurações**, permitindo personalização total:

- 🎨 **Temas de Cores**  
Personalize o esquema de cores da interface.

- 🖥️ **Estilo das Bordas da Box**  
Altere o layout visual das boxes e janelas.

- 👤 **Configurações de Usuários UID 1000 e Demais**  
Defina regras específicas para o primeiro usuário real (UID 1000) e outros.

- 🚀 **Modo Otimizado (Modo Simples)**  
Desativa elementos visuais para melhor performance em servidores com poucos recursos.

- ⏱️ **Tempo de Atualização do Limite e Monitor**  
Ajuste os intervalos de atualização dos módulos de **controle de limite** e **monitoramento de sessões**.

- ⚡ **Outras Configurações Avançadas**  
Incluindo opções de desempenho, segurança e comportamento do sistema.

---

## 📂 Estrutura e Dependências

O ArkSH depende apenas dos seguintes diretórios internos:

```
/opt/arksh/config
/opt/arksh/effect
/opt/arksh/print
```

Não requer bancos de dados externos ou serviços adicionais.

---

## ✅ Requisitos Mínimos

- Sistema Linux funcional (Debian, Ubuntu, etc).
- Serviços de rede (ex.: SSH, Dropbear, OpenVPN) devidamente instalados e ativos.
- Permissão de root para execução.

---

## 📣 Observações Importantes

- **Usuários criados apenas dentro de bancos de dados externos de outros painéis não aparecerão no ArkSH**, pois o sistema lê apenas os arquivos reais do sistema.

- Por segurança, qualquer alteração nos limites de conexão afeta apenas usuários **com UID acima de 1000**.

- O ArkSH foi projetado para **não sobrescrever nem interferir nas configurações de outros gerenciadores**.

---

## 📞 Suporte e Contato

Para dúvidas, sugestões ou suporte:  
**[Seu contato / Telegram / GitHub / Site]**

---

> Desenvolvido por Vinícius Araújo  
> © 2025 - Todos os direitos reservados.
