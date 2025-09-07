# Trabalho Prático: Sistema de Roteamento para Consultas Turísticas

## 1. Objetivo do Projeto

Desenvolver um sistema capaz de, a partir de uma consulta de um turista, classificar a intenção da pergunta e direcioná-la para a cadeia de processamento mais adequada. O sistema deve permitir:

- **Roteiros personalizados:** Gerar sugestões de itinerário com base no perfil do turista (ex: aventura, cultural, gastronômico).
- **Módulos especializados por função:** Utilizar cadeias de processamento dedicadas a diferentes tipos de consulta (ex: informações sobre locais, logística de transporte, detalhes de roteiro). **Atenção:** Não serão utilizados Agentes do LangChain, mas sim Cadeias (Chains) específicas, orquestradas por um roteador.
- **Geração rápida e automatizada:** Otimizar a velocidade de resposta utilizando um modelo de inferência de alto desempenho como o Groq.
- **Estrutura escalável e personalizável:** Permitir fácil adição de novas funcionalidades ou bases de conhecimento.

---

## 2. Tecnologias Envolvidas

- **LangChain:** Framework principal para orquestrar as cadeias de processamento e a lógica de roteamento.
- **Groq:** Motor de inferência para o Large Language Model (LLM), otimizado para alta velocidade.
- **Router Chain (LangChain):** Componente central responsável por analisar a consulta do usuário e decidir qual cadeia especializada deve processá-la.
- **Pinecone:** Base de dados vetorial para implementar o RAG, populada com informações sobre destinos turísticos, pontos de interesse, restaurantes e eventos locais.
- **RAG (Retrieval-Augmented Generation):** Permite ao sistema acessar informações atualizadas e específicas, garantindo precisão nas respostas.

---

## 3. Estrutura do Projeto

O sistema é composto por módulos lógicos:

- **Módulo de Entrada:** Recebe a consulta do usuário (ex: "roteiro cultural em Paris por 3 dias", "como chegar ao Coliseu?", "quais são os melhores restaurantes veganos em Tóquio?").
- **Router Chain:** Classifica a intenção do usuário. Exemplos de classificações:
  - `roteiro-viagem`
  - `logistica-transporte`
  - `info-local`
  - `traducao-idiomas`
- **Cadeias Especializadas:**
  - **Itinerary Chain (roteiro-viagem):** Recebe o perfil do turista (se disponível), utiliza o RAG para buscar informações sobre atrações e eventos e gera um roteiro detalhado.
  - **Logistics Chain (logistica-transporte):** Responde a perguntas sobre transporte, acomodação e outros aspectos práticos da viagem.
  - **Local Info Chain (info-local):** Fornece informações específicas sobre pontos turísticos, restaurantes, horários de funcionamento, etc., usando o RAG.
  - **Translation Chain (traducao-idiomas):** (Bônus) Guia de tradução, fornecendo frases úteis para a viagem com base na solicitação do usuário.
- **Base de Conhecimento (RAG):** Exemplo de dados sobre cidades turísticas (ex: Rio de Janeiro e Paris) para indexação no Pinecone, incluindo pontos turísticos, restaurantes, dicas de segurança, etc.

---

## 4. Requisitos e Entrega

- **Código-fonte:** Repositório no GitHub contendo todo o código do projeto, bem comentado e organizado.
- **Demonstração:** Vídeo de 1 a 3 minutos mostrando a funcionalidade do sistema em ação, demonstrando os diferentes fluxos de roteamento e a capacidade de RAG.
