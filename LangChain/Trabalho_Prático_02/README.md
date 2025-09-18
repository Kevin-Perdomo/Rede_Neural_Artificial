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
├── 📄 requirements.txt          # Dependências Python
├── 🔐 .env                      # Chaves de API (privado)
├── 🚫 .gitignore               # Proteção do .env
└── 📁 docs/                     # Documentação
    ├── 📋 PROBLEMA.md           # Especificação
    └── 🔧 SOLUCAO.md            # Implementação
```

> 🔐 **Segurança:** O arquivo `.env` contém as chaves privadas de API e está protegido pelo `.gitignore` para nunca ser enviado ao repositório público.

---

## ⚡ **Execução Rápida**

### **🐍 Pré-requisitos: Anaconda**

```bash
# 1. Download e instalação do Anaconda
# https://www.anaconda.com/products/distribution
wget https://repo.anaconda.com/archive/Anaconda3-2023.09-Linux-x86_64.sh
bash Anaconda3-2023.09-Linux-x86_64.sh
```

### **🚀 Setup do Ambiente:**

```bash
# 2. Criar ambiente conda dedicado
conda create -n LangChain python=3.11 -y

# 3. Ativar o ambiente
conda activate LangChain

# 4. Instalar dependências no ambiente
pip install -r requirements.txt

# 5. Criar kernel Jupyter para VS Code
python -m ipykernel install --user --name=LangChain --display-name="LangChain"

# 6. Configurar variáveis de ambiente (.env)
GROQ_API_KEY=sua_chave_groq
PINECONE_API_KEY=sua_chave_pinecone
```

### **🔧 Gerenciamento do Ambiente:**

```bash
# Ativar ambiente LangChain
conda activate LangChain

# Desativar ambiente
conda deactivate

# Listar ambientes disponíveis
conda env list

# Verificar kernel no Jupyter
jupyter kernelspec list
```

### **📝 Configuração VS Code:**

1. **Abrir notebook** (.ipynb)
2. **Selecionar Kernel** → `LangChain` (canto superior direito)
3. **Verificar ambiente** ativo na barra de status

> 🎯 **Framework Unificado:** Todo o projeto utiliza o **LangChain** como framework principal, integrando Groq (LLM), Pinecone (vetores) e HuggingFace (embeddings) sob uma única arquitetura coesa.

### **2️⃣ Executar:**

```python
# Ativar ambiente primeiro
# conda activate LangChain

# Interface simplificada
resposta = perguntar_guia("O que visitar no Rio de Janeiro?")
print(resposta)
```

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
