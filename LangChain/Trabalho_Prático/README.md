# 🚀 **Sistema de Guia Turístico Inteligente**

> **Trabalho Prático - Redes Neurais Artificiais**

## 📓 **Aluno**

**Sistema de Guia Turístico Inteligente**  
**LangChain + Router Chain + RAG para classificação turística**  
**Desenvolvido por: Kevin Siqueira Perdomo**  
**Matrícula: 201911250205**  
**Curso: Bacharelado em Engenharia De Computação**  
📧 **Email:** kevin.siqueira23@gmail.com  
🐙 **GitHub:** [Kevin-Perdomo](https://github.com/Kevin-Perdomo)

---> **Tecnologias:** LangChain + Groq + Pinecone + RAG

---

## 🎯 **Visão Geral**

Sistema inteligente que classifica consultas turísticas e as direciona para especialistas dedicados, utilizando **Router Chain** + **4 Chains Especializadas** + **RAG** para fornecer respostas contextualizadas sobre turismo.

### **🏆 Destaques:**

- ⚡ **91.7% de precisão** na classificação de intenções
- 🗺️ **4 especialistas** (Roteiros, Logística, Info Local, Tradução)
- 📊 **Base vetorial** com dados reais (Rio + Paris)
- 💬 **Interface unificada** pronta para uso

---

## 📚 **Documentação**

### **📋 Especificação do Problema**

➡️ **[Ver PROBLEMA.md](./docs/PROBLEMA.md)**

- Requisitos do professor
- Stack tecnológico obrigatório
- Critérios de avaliação

### **🔧 Solução Implementada**

➡️ **[Ver SOLUCAO.md](./docs/SOLUCAO.md)**

- Arquitetura técnica completa
- Métricas de performance
- Funcionalidades implementadas

---

## 🏗️ **Estrutura do Projeto**

```
📁 Guia_de_Viagem/
├── 📓 01-Pinecone.ipynb         # Base vetorial + RAG
├── 📓 02-RAG.ipynb              # Sistema de recuperação
├── 📓 03-Chains.ipynb           # 4 especialistas
├── 📓 04-Router.ipynb           # Classificador inteligente
├── 📓 05-Sistema.ipynb          # Interface unificada
├── 📄 base_conhecimento.txt     # Dados turísticos
├── 📄 requirements.txt          # Dependências
└── 📁 docs/                     # Documentação
    ├── 📋 PROBLEMA.md           # Especificação
    └── 🔧 SOLUCAO.md            # Implementação
```

---

## ⚡ **Execução Rápida**

### **1️⃣ Setup:**

```bash
# Instalar dependências
pip install -r requirements.txt

# Configurar variáveis de ambiente (.env)
GROQ_API_KEY=sua_chave_groq
PINECONE_API_KEY=sua_chave_pinecone
```

### **2️⃣ Executar:**

```python
# Interface simplificada
resposta = perguntar_guia("O que visitar no Rio de Janeiro?")
print(resposta)
```

### **3️⃣ Notebooks:**

1. **01-Pinecone.ipynb** → Indexar dados
2. **05-Sistema.ipynb** → Interface completa

---

## 🎬 **Demo**

### **Exemplos de Uso:**

```python
# Roteiros
"Principais pontos turísticos de Paris" → 🗺️ Especialista Roteiros

# Logística
"Como ir do aeroporto ao centro?" → 🚗 Especialista Logística

# Cultura Local
"Costumes franceses importantes" → 📍 Especialista Info Local

# Tradução
"Como dizer 'obrigado' em francês?" → 🌐 Especialista Tradução
```

---

## 📊 **Métricas**

| Componente | Performance     | Status |
| ---------- | --------------- | ------ |
| **Router** | 91.7% precisão  | ✅     |
| **RAG**    | ~500ms busca    | ✅     |
| **Chains** | 4 especialistas | ✅     |
| **Base**   | 40+ documentos  | ✅     |

---

## 🛠️ **Stack Técnico**

- **🦜 LangChain:** Orquestração (sintaxe moderna)
- **⚡ Groq:** LLM alta performance
- **📊 Pinecone:** Base vetorial
- **🤗 HuggingFace:** Embeddings
- **🐍 Python:** Jupyter Notebooks

---

_Sistema completo de turismo inteligente com classificação automática e especialistas dedicados._
