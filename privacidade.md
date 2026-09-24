---
title: Política de Privacidade — CysOT Radar
---
# Política de Privacidade — CysOT Radar de Exposição

**Última atualização:** 24 de setembro de 2026
**Responsável:** CysOT
**Contato:** privacidade@cysot.com.br

---

## Resumo em uma frase

O CysOT Radar **não coleta, não armazena e não transmite dados pessoais**. Não
temos servidor: tudo o que o aplicativo guarda fica no seu aparelho.

---

## 1. Quem somos

O CysOT Radar de Exposição é um aplicativo de cibersegurança industrial que
verifica, de forma passiva, se um ativo de automação (CLP, IHM, SCADA, RTU,
gateway) está visível na internet.

O aplicativo **não possui servidor próprio, backend ou banco de dados na
nuvem**. Não existe cadastro, login ou conta de usuário.

---

## 2. Dados que NÃO coletamos

Para ser explícito, o aplicativo **não coleta**:

- Nome, e-mail, telefone ou qualquer identificador pessoal
- Localização do dispositivo
- Contatos, fotos, arquivos, microfone ou câmera
- Identificadores de publicidade ou rastreamento
- Dados de uso, telemetria, analytics ou relatórios de falha
- Endereço IP do usuário (registrado apenas pelas fontes de terceiros que o
  aplicativo consulta, conforme a política de cada uma)

Não há SDK de publicidade, analytics ou rastreamento embarcado.

---

## 3. Dados armazenados no seu aparelho

Tudo abaixo fica **exclusivamente no armazenamento privado do aplicativo**, no
seu dispositivo, e nunca é enviado a nós:

| Dado | Onde fica | Por quê |
|---|---|---|
| Chaves de API das fontes | **Keychain (iOS) / Keystore (Android)**, cifradas | Autenticar consultas às fontes que você escolher usar |
| Histórico de verificações | Armazenamento privado do app | Comparar verificações e detectar mudanças |
| Inventário de ativos | Armazenamento privado do app | Monitorar endereços ao longo do tempo |
| Preferências (tema, setor, tempo limite) | Armazenamento privado do app | Manter sua configuração |

**Backup desativado.** O aplicativo desabilita explicitamente o backup para
nuvem e a transferência entre dispositivos (Android: `allowBackup=false` e
regras de extração de dados; iOS: chaves marcadas como não sincronizáveis com o
iCloud). Seus dados não saem do aparelho nem por backup.

**Como apagar:** desinstalar o aplicativo remove tudo. Em Ajustes › Dados
locais você também pode limpar o histórico e remover as chaves a qualquer
momento.

---

## 4. Consultas a serviços de terceiros

Quando você verifica um endereço, o aplicativo envia **apenas esse endereço IP**
para as bases públicas de OSINT que estiverem ativas. Nenhum dado seu acompanha
a consulta — nem identificador, nem localização, nem histórico.

Fontes consultadas e suas políticas:

| Fonte | Política de privacidade |
|---|---|
| Shodan | https://www.shodan.io/legal/privacy |
| Netlas.io | https://netlas.io/privacy_policy/ |
| urlscan.io | https://urlscan.io/docs/privacy/ |
| SANS Internet Storm Center | https://isc.sans.edu/privacy.html |
| AlienVault OTX | https://cybersecurity.att.com/privacy-policy |
| RDAP (RIRs: LACNIC, ARIN, RIPE) | política do RIR responsável pelo bloco |
| RIPEstat | https://www.ripe.net/about-us/legal/ripe-ncc-privacy-statement/ |
| ipwho.is | https://ipwho.is/privacy |
| Censys | https://about.censys.io/privacy-policy/ |
| Criminal IP | https://www.criminalip.io/privacy |
| ONYPHE | https://www.onyphe.io/privacy |
| BinaryEdge | https://www.binaryedge.io/privacy.html |
| LeakIX | https://leakix.net/legal |
| ZoomEye | https://www.zoomeye.ai/privacy |
| GreyNoise | https://www.greynoise.io/privacy-policy |
| AbuseIPDB | https://www.abuseipdb.com/legal |
| VirusTotal | https://docs.virustotal.com/docs/privacy-policy |

Resolução de nomes de host usa o DNS-over-HTTPS da Cloudflare
(https://www.cloudflare.com/privacypolicy/). A descoberta do seu IP público
usa o ipify (https://www.ipify.org/).

Ao usar essas fontes você fica sujeito às políticas delas. Desative qualquer
fonte em Ajustes se não quiser consultá-la.

---

## 5. Suas chaves de API

Se você cadastrar uma chave de API (Shodan, Censys, VirusTotal etc.):

- Ela é gravada **cifrada** no cofre do sistema operacional
- É enviada **somente** para a própria fonte que ela autentica, sobre HTTPS
- **Nunca** é enviada para a CysOT ou para qualquer outro destino
- Pode ser removida a qualquer momento em Ajustes › Fontes

---

## 6. Segurança

- Todo o tráfego usa **HTTPS**; tráfego em texto claro é bloqueado por política
  de rede no Android e por App Transport Security no iOS
- No Android, certificados instalados pelo usuário não são aceitos em produção,
  o que impede interceptação por proxy
- As credenciais ficam em armazenamento cifrado respaldado por hardware quando
  o aparelho oferece esse recurso
- O aplicativo não solicita permissões sensíveis: apenas acesso à internet

---

## 7. Crianças

O aplicativo é uma ferramenta profissional de cibersegurança industrial, não se
destina a menores de 18 anos e não coleta dados de crianças.

---

## 8. Seus direitos (LGPD e GDPR)

Como não coletamos nem tratamos dados pessoais, não há dados sob nossa custódia
para acessar, corrigir, portar ou excluir. Os dados gerados pelo uso ficam sob
seu controle exclusivo, no seu aparelho.

Dúvidas sobre este documento: **privacidade@cysot.com.br**

---

## 9. Uso responsável

O aplicativo consulta registros públicos sobre endereços IP — atividade
legítima e não invasiva. Ainda assim, utilize-o apenas sobre ativos da sua
organização ou de clientes que autorizaram formalmente o trabalho.

---

## 10. Alterações

Mudanças relevantes nesta política serão publicadas nesta página com nova data
de atualização e, quando cabível, comunicadas na própria loja.
