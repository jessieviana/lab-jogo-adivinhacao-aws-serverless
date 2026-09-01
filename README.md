# 🎯 Jogo de Adivinhação · AWS Serverless

```
╔══════════════════════════════════════════════════════════════╗
║  Lambda → API Gateway → S3 · arquitetura 100% serverless    ║
╚══════════════════════════════════════════════════════════════╝
```

> Lab desenvolvido durante o programa **AWS Developer Associate**  
> na [Escola da Nuvem](https://escoladanuvem.org/) ☁️

---

## `// arquitetura`

```
  usuário
     │
     ▼
┌─────────────┐     GET /jogo     ┌───────────────┐     invoke     ┌──────────────┐
│  Amazon S3  │ ───────────────►  │  API Gateway  │ ────────────►  │  AWS Lambda  │
│  (frontend) │                   │  (HTTP API)   │                │  (Python)    │
└─────────────┘                   └───────────────┘                └──────────────┘
  site estático                    roteamento                       lógica do jogo
```

---

## `// stack`

![AWS Lambda](https://img.shields.io/badge/AWS_Lambda-0d1117?style=flat-square&logo=amazonwebservices&logoColor=FF9900)
![API Gateway](https://img.shields.io/badge/API_Gateway-0d1117?style=flat-square&logo=amazonwebservices&logoColor=FF9900)
![Amazon S3](https://img.shields.io/badge/Amazon_S3-0d1117?style=flat-square&logo=amazonwebservices&logoColor=FF9900)
![Python](https://img.shields.io/badge/Python_3.13-0d1117?style=flat-square&logo=python&logoColor=3776AB)
![HTML](https://img.shields.io/badge/HTML-0d1117?style=flat-square&logo=html5&logoColor=E34F26)

---

## `// como funciona`

```
[1] Usuário acessa o site hospedado no S3
[2] Digita um número de 1 a 10 e clica em "Enviar"
[3] O frontend faz um GET para a API Gateway
[4] A API Gateway aciona a função Lambda
[5] O Lambda processa e retorna: acertou ou errou
[6] Resultado exibido na tela em tempo real
```

---

## `// serviços configurados`

```
┌──────────────────────────────────────┬─────────────────────────────┐
│ SERVIÇO                              │ CONFIGURAÇÃO                │
├──────────────────────────────────────┼─────────────────────────────┤
│ AWS Lambda                           │ Python 3.13 · zip deploy    │
│ Amazon API Gateway                   │ HTTP API · rota GET /jogo   │
│ Amazon S3                            │ static website · público    │
│ CORS                                 │ origin: * · method: GET     │
│ IAM                                  │ permissões Lambda + S3      │
└──────────────────────────────────────┴─────────────────────────────┘
```

---

## `// o que aprendi`

```bash
[OK] Criar e deployar função Lambda com Python
[OK] Expor Lambda via API Gateway HTTP com rota GET
[OK] Configurar CORS para comunicação cross-origin
[OK] Hospedar frontend estático no S3
[OK] Liberar acesso público via Bucket Policy (JSON)
[OK] Integrar S3 + API Gateway + Lambda end-to-end
[OK] Identificar recursos AWS via ARN
```

---

## `// créditos`

Lab desenvolvido como parte do **AWS Developer Associate (DVA-C02)**  
na **Escola da Nuvem** em parceria com a **AWS**.

---

<div align="center">

`jessie viana. · cloud · Rio de Janeiro`

</div>
