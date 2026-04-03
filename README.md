# Chatbot para Triagem Hospitalar - IBM Watson Assistant

Projeto acadêmico de IA voltado à automação de atendimento inicial em contexto hospitalar, com foco em triagem, FAQ institucional e experiência conversacional para o Hospital das Clínicas.

## Visão geral

Este repositório concentra artefatos de um chatbot construído com **IBM Watson Assistant**, além de uma interface web simples em **HTML** para embed do assistente. O projeto foi estruturado para responder dúvidas frequentes de pacientes e visitantes, com fluxos ligados a temas como:

- localização do hospital
- documentos necessários para atendimento
- resultados de exames
- informações gerais de suporte ao usuário
- fluxos conversacionais auxiliares e variações de diálogo

A interface web atual é enxuta: o `index.html` renderiza uma página de boas-vindas e injeta o script do Watson Assistant com `integrationID`, `region` e `serviceInstanceID` configurados para o widget web. O título da página é `Watson`, há um cabeçalho “Bem-vindo ao Assistente Virtual do HC” e um parágrafo informando que se trata de um chatbot para atendimento hospitalar automatizado.

## Objetivo do projeto

O objetivo principal é demonstrar uma solução de **atendimento automatizado com IA conversacional** para reduzir dúvidas recorrentes e melhorar a navegação do usuário em um ambiente hospitalar.

Pelos arquivos de diálogo do repositório, o bot cobre intenções relacionadas a:
- **resultados de exames/consultas**
- **localização**
- **documentos para atendimento**
- **fluxos conversacionais de ajuda e suporte**

## Tecnologias e componentes

- **IBM Watson Assistant** para modelagem conversacional e publicação do assistente
- **HTML5** para a interface web de incorporação do chat widget
- **JSON** para armazenamento/exportação dos fluxos, intents e configurações conversacionais

## Estrutura atual do repositório

```text
ai-sprint-privado/
├── Bot_Hospital-Clinicas-dialog.json
├── HospitalClinicas_Dialog_Ajuda.json
├── flows-ai-sprint.json
├── fluxo-chatbot.json
├── index.html
├── integrantes.txt
└── video-teste.txt
```

### Descrição dos principais arquivos

- `index.html`  
  Página web simples que incorpora o widget do IBM Watson Assistant.

- `Bot_Hospital-Clinicas-dialog.json`  
  Arquivo principal de diálogo com intents, exemplos e entidades relacionadas ao atendimento hospitalar.

- `HospitalClinicas_Dialog_Ajuda.json`  
  Variação/apoio de diálogo com intents semelhantes e cobertura complementar de perguntas frequentes.

- `flows-ai-sprint.json`  
  Arquivo de fluxo conversacional exportado do ambiente de IA.

- `fluxo-chatbot.json`  
  Estrutura adicional de fluxo do chatbot.

- `integrantes.txt`  
  Arquivo de apoio com informações dos participantes.

- `video-teste.txt`  
  Referência usada para entrega/apresentação do projeto.

## Funcionalidades mapeadas

### 1. Informações de localização

O bot responde perguntas sobre endereço, bairro, cidade, CEP e localização do hospital.

### 2. Documentação para atendimento

Há cobertura para dúvidas sobre RG, CPF, receita/guia médica, comprovante de agendamento e cartão do SUS. Além dos exemplos de perguntas, o projeto usa sinônimos e padrões para enriquecer o reconhecimento dessas entradas.

### 3. Consulta de resultados

O diálogo inclui intenção para consulta de resultados, cobrindo perguntas sobre laudos e exames, como ressonância, tomografia, raio-x e exames laboratoriais.

### 4. Atendimento conversacional via web

A camada web atual é propositalmente simples e serve como ponto de entrada para o assistente, permitindo embutir a solução em página HTML e renderizar o chat widget diretamente no navegador.

## Como executar localmente

### Pré-requisitos

- navegador web moderno
- acesso a uma instância válida do **IBM Watson Assistant**
- credenciais/IDs válidos de integração do chat widget

### Passos

1. Clone o repositório:

```bash
git clone https://github.com/matheusmoyaoliveira/ai-sprint-privado.git
cd ai-sprint-privado
```

2. Abra o arquivo `index.html` no navegador.

3. Verifique se as configurações do Watson Assistant no bloco JavaScript estão corretas para a sua instância.

## Trecho técnico relevante

O `index.html` configura o objeto `window.watsonAssistantChatOptions` e carrega dinamicamente `WatsonAssistantChatEntry.js`, renderizando o widget ao abrir a página.

## Possíveis melhorias técnicas

Para evoluir esse projeto e deixá-lo mais forte para portfólio, os próximos passos recomendados são:

- separar claramente **documentação funcional** e **documentação técnica**
- adicionar prints ou GIFs do chatbot em funcionamento
- documentar as **intenções**, **entidades** e **casos de uso principais**
- incluir um diagrama simples do fluxo conversacional
- versionar melhor os arquivos exportados do Watson Assistant
- publicar uma demo estática ou instrução objetiva de execução
- padronizar nomenclatura dos arquivos JSON
- criar uma seção de **arquitetura da solução**

## Autor

**Matheus Moya de Oliveira**  
Estudante de Análise e Desenvolvimento de Sistemas, com foco em Back-End, automação, APIs e projetos aplicados a problemas reais.
