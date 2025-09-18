# 📋 **Especificação do Problema**

> **Trabalho Prático proposto pelo Professor**  
> **Disciplina:** Redes Neurais Artificiais  
> **Tema:** Sistema de Roteamento para Consultas Turísticas

---

## 🎯 **1. Objetivo do Projeto**

Desenvolver um sistema capaz de, a partir de uma consulta de um turista, classificar a intenção da pergunta e direcioná-la para a cadeia de processamento mais adequada. O sistema deve permitir:

### **Funcionalidades Requeridas:**

- **🗺️ Roteiros personalizados:** Gerar sugestões de itinerário com base no perfil do turista (ex: aventura, cultural, gastronômico).

- **⛓️ Módulos especializados por função:** Utilizar cadeias de processamento dedicadas a diferentes tipos de consulta (ex: informações sobre locais, logística de transporte, detalhes de roteiro).

  > **⚠️ Restrição Importante:** Não serão utilizados Agentes do LangChain, mas sim **Cadeias (Chains)** específicas, orquestradas por um roteador.

- **⚡ Geração rápida e automatizada:** Otimizar a velocidade de resposta utilizando um modelo de inferência de alto desempenho como o Groq.

- **🔧 Estrutura escalável e personalizável:** Permitir fácil adição de novas funcionalidades ou bases de conhecimento.

---

## 🛠️ **2. Tecnologias Envolvidas**

### **Stack Tecnológico Obrigatório:**

- **🦜 LangChain:** Framework principal para orquestrar as cadeias de processamento e a lógica de roteamento.

- **⚡ Groq:** Motor de inferência para o Large Language Model (LLM), otimizado para alta velocidade.

- **🎯 Router Chain (LangChain):** Componente central responsável por analisar a consulta do usuário e decidir qual cadeia especializada deve processá-la.

- **📊 Pinecone:** Base de dados vetorial para implementar o RAG, populada com informações sobre destinos turísticos, pontos de interesse, restaurantes e eventos locais.

- **🔍 RAG (Retrieval-Augmented Generation):** Permite ao sistema acessar informações atualizadas e específicas, garantindo precisão nas respostas.

---

## 🏗️ **3. Estrutura Arquitetural Requerida**

### **Módulos Lógicos:**

#### **📥 Módulo de Entrada**

Recebe a consulta do usuário com exemplos como:

- _"roteiro cultural em Paris por 3 dias"_
- _"como chegar ao Coliseu?"_
- _"quais são os melhores restaurantes veganos em Tóquio?"_

#### **🎯 Router Chain**

Classifica a intenção do usuário. Exemplos de classificações obrigatórias:

- `roteiro-viagem`
- `logistica-transporte`
- `info-local`
- `traducao-idiomas`

#### **⛓️ Cadeias Especializadas**

1. **🗺️ Itinerary Chain (`roteiro-viagem`)**

   - Recebe o perfil do turista (se disponível)
   - Utiliza o RAG para buscar informações sobre atrações e eventos
   - Gera um roteiro detalhado

2. **🚗 Logistics Chain (`logistica-transporte`)**

   - Responde perguntas sobre transporte
   - Informações sobre acomodação
   - Aspectos práticos da viagem

3. **📍 Local Info Chain (`info-local`)**

   - Informações específicas sobre pontos turísticos
   - Restaurantes e horários de funcionamento
   - Utiliza RAG para dados atualizados

4. **🌐 Translation Chain (`traducao-idiomas`)** **(Bônus)**
   - Guia de tradução
   - Frases úteis para viagem
   - Baseado na solicitação do usuário

#### **📚 Base de Conhecimento (RAG)**

Dados sobre cidades turísticas para indexação no Pinecone:

- **Exemplo:** Rio de Janeiro e Paris
- **Conteúdo:** Pontos turísticos, restaurantes, dicas de segurança, etc.

---

## 📦 **4. Requisitos de Entrega**

### **Entregáveis Obrigatórios:**

- **💻 Código-fonte:** Repositório no GitHub contendo todo o código do projeto, bem comentado e organizado.

- **🎬 Demonstração:** Vídeo de **1 a 3 minutos** mostrando:
  - Funcionalidade do sistema em ação
  - Diferentes fluxos de roteamento
  - Capacidade de RAG demonstrada

### **Critérios de Avaliação:**

- ✅ Implementação correta do Router Chain
- ✅ Funcionamento das Cadeias Especializadas
- ✅ Integração efetiva do RAG com Pinecone
- ✅ Performance com Groq
- ✅ Organização e documentação do código
- ✅ Qualidade da demonstração em vídeo

---

## 🎯 **Resumo dos Desafios Técnicos**

1. **Classificação Inteligente:** Implementar Router Chain preciso para intenções
2. **Especialização:** Criar Chains dedicadas por domínio
3. **RAG Eficiente:** Integrar Pinecone para recuperação contextual
4. **Performance:** Utilizar Groq para inferência rápida
5. **Escalabilidade:** Arquitetura flexível para expansão

---

_Documento baseado na especificação original do professor_
