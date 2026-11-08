# DCEng Pro — documentação

Documentação pública da **DCEng Pro**, a área de membros da DCEng Engenharia (Brasília/DF)
para profissionais que orçam obra e manutenção predial.

![DCEng Engenharia](logo/light.svg)

- **Produto:** <https://pro.dce.eng.br>
- **Área de membros:** <https://pro.dce.eng.br/membros>
- **Contato:** contato@dce.eng.br

## O que é este repositório

Aqui ficam **somente** os textos da documentação do produto: como criar a conta, o que cada plano
inclui, como usar cada ferramenta, como funciona a cobrança, o que fazemos para proteger a conta e
quais são os limites do que a ferramenta entrega.

Este repositório **não** contém — e não deve conter — código do produto, credenciais, detalhes de
infraestrutura, dados de clientes ou qualquer material interno.

## Estrutura

```
.
├── docs.json              # configuração do site (Mintlify)
├── index.mdx              # introdução (página inicial)
├── inicio-rapido.mdx
├── planos.mdx
├── ferramentas/           # calculadora, SINAPI, BDI, comparador, PDF
├── conta/                 # acesso, segurança, equipe, assinatura
├── conhecimento/          # cursos e comunidade
├── dados/                 # privacidade
├── limites.mdx
├── suporte.mdx
├── changelog.mdx
├── logo/                  # marca (light, dark e favicon)
├── custom.css             # ajustes visuais da marca
├── SECURITY.md            # como relatar um problema de segurança
└── README.md
```

## Pré-visualizar localmente

Requer Node.js 18 ou superior.

```bash
npm i -g mintlify
mintlify dev
```

Abra `http://localhost:3000`.

Pré-requisito de conteúdo: `docs.json` válido. O arquivo segue o schema oficial
(`https://mintlify.com/docs.json`); qualquer chave fora do schema impede o build.

## Publicar

O site é publicado pela integração da Mintlify com este repositório: o que entra na branch `main`
vai para o ar. Para ativar, o responsável da DCEng instala o aplicativo da Mintlify na conta do
GitHub e aponta o domínio (`docs.dce.eng.br`). Enquanto isso não for feito, este repositório serve
como fonte única do texto.

O `llms.txt` do site é gerado pela própria Mintlify — não precisa ser mantido à mão.

## Regras de publicação (sigilo)

Antes de abrir um pull request, confira que o texto **não** traz:

- nome, e-mail, telefone ou qualquer dado de cliente ou membro;
- chave de API, token, senha, variável de ambiente ou trecho de configuração;
- nome de gateway de pagamento, de provedor de infraestrutura ou de banco de dados;
- caminho de servidor, nome de tabela, estrutura de pastas interna ou print de painel administrativo;
- número de registro profissional (CREA), CNPJ ou CPF;
- promessa de prazo, de resultado, de preço futuro ou de conformidade normativa.

O tom é técnico e direto, em português do Brasil. Nada de "garantimos", "o melhor", "com certeza".

## Quem aprova

Toda alteração de conteúdo passa pelo responsável técnico da DCEng antes de ir para a `main`.
Alteração de preço, de plano ou de texto legal só entra depois de publicada na fonte oficial
(página de planos e Termos de Uso).
