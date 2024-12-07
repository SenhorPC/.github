# Automação de Gestão para Suporte Técnico Informático

## Descrição

Este projeto visa desenvolver uma automação para gerenciar e operacionalizar uma pequena empresa de suporte técnico informático.
Nosso objetivo é automatizar atividades antes executadas por humanos, para serem executadas por assistentes/agentes AI.
O foco inicial será pelas atividades secundárias, por exemplo:
- Se você é um técnico de suporte, essa é sua atividade principal. Então o foco inicial será complementar nas área em que não seu expertise, como:
  - Vendas
  - Finanças
  - Gestão Estratégica de Crescimento
  - Suporte Técnico

### Tecnologias Utilizadas

- **N8N**: Plataforma de automação de workflows.
- **PostgreSQL**: Banco de dados relacional requerido pelo N8N.
- **Redis**: Armazenamento em memória para gerenciamento de sessões.
- **Gmail**: Recebimento de pedidos dos clientes/leads e comunicação.
- **WhatsApp**: Recebimento de pedidos dos clientes/leads e comunicação.
- **Zapster**: Acesso ao Whatsapp via API.
- **OpenAI Assistant**: Assistentes/agentes para interação humana.

## Estrutura do Repositório

- `src/`: Scripts e configurações do projeto.
- `docs/`: Documentação do projeto, incluindo guias e changelogs.
- `.github/`: Configurações do GitHub, incluindo workflows.

## Como Contribuir

Para colaboradores externos:

1. Faça um fork do repositório.
2. Crie uma branch para sua feature ou correção (`git checkout -b feature/nome-da-feature`).
3. Faça suas alterações e commit (`git commit -m 'Adiciona nova feature'`).
4. Envie para o seu fork (`git push origin feature/nome-da-feature`).
5. Crie um Pull Request.

Para a equipe SenhorPC:

- Crie uma nova branch para cada alteração significativa.
- Utilize Pull Requests para revisão e integração das alterações no `main`.
- Documente as alterações no changelog e atualize a versão conforme necessário.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
