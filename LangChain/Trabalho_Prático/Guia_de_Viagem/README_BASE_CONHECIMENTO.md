# 🚀 Sistema Turístico Inteligente - Base de Conhecimento

## 📁 **Estrutura de Arquivos**

```
Guia_de_Viagem/
├── 01-Pinecone.ipynb              # Base vetorial
├── 02-RAG.ipynb                   # Sistema de recuperação
├── 03-Chains.ipynb                # Chains especializadas
├── 04-Router.ipynb                # Roteamento inteligente
├── 05-Sistema.ipynb               # Interface completa
├── base_conhecimento.txt          # ⭐ Base de dados centralizada
└── README.md                      # Esta documentação
```

## 🎯 **Base de Conhecimento Centralizada**

### ✅ **Vantagens da Nova Abordagem:**

1. **📝 Manutenção Simples**: Um único arquivo `base_conhecimento.txt` para todos os dados
2. **🔄 Reutilização**: Mesmos dados usados em todos os notebooks
3. **📊 Consistência**: Informações sempre atualizadas em todos os lugares
4. **🛠️ Profissional**: Separação clara entre código e dados
5. **📈 Escalabilidade**: Fácil adição de novas cidades/informações

### 📋 **Formato do Arquivo base_conhecimento.txt:**

```txt
# 🏖️ BASE DE CONHECIMENTO TURÍSTICO - RIO DE JANEIRO

## ROTEIROS - RIO
Cristo Redentor: Uma das Sete Maravilhas do Mundo Moderno...
Pão de Açúcar: Bondinho famoso com vista panorâmica...

## LOGÍSTICA - RIO
Aeroporto Galeão: Principal aeroporto internacional...
Metro Rio: Linhas 1, 2 e 4 conectam principais pontos...

# 🗼 BASE DE CONHECIMENTO TURÍSTICO - PARIS

## ROTEIROS - PARIS
Torre Eiffel: Símbolo de Paris, 324m de altura...
Museu do Louvre: Maior museu do mundo...

## LOGÍSTICA - PARIS
Charles de Gaulle: Principal aeroporto...
Metro Paris: 14 linhas disponíveis...
```

## 🔧 **Como Usar**

### **1. Em Notebooks - Função Integrada:**

```python
# Função já definida na célula do notebook
def carregar_base_conhecimento(arquivo_path="base_conhecimento.txt"):
    # ... código da função ...

# Carregar dados
dados = carregar_base_conhecimento()
print(f"Total de documentos: {sum(len(docs) for docs in dados.values())}")
```

### **2. Autocontido - Sem Dependências:**

```python
# Cada notebook tem sua própria função de carregamento
# Não precisa importar nenhum arquivo externo
# Fallback automático se base_conhecimento.txt não existir
```

### **3. Para Chains - Função no Notebook:**

```python
# Função específica definida no notebook 03
def carregar_base_conhecimento_chains(arquivo_path="base_conhecimento.txt"):
    # ... código adaptado para chains ...

# Uso direto
contextos = carregar_base_conhecimento_chains()
# Resultado: {"roteiro": {"rio": [...], "paris": [...]}, "logistica": {...}}
```

## 📊 **Notebooks Atualizados**

| Notebook              | Status | Modificação                                |
| --------------------- | ------ | ------------------------------------------ |
| **01-Pinecone.ipynb** | ✅     | Carrega dados do arquivo para indexação    |
| **02-RAG.ipynb**      | ✅     | Usa dados do Pinecone (já atualizado)      |
| **03-Chains.ipynb**   | ✅     | Simula RAG com dados do arquivo            |
| **04-Router.ipynb**   | ✅     | Sistema independente (sem dados hardcoded) |
| **05-Sistema.ipynb**  | ✅     | Integra tudo usando Pinecone               |

## 🛠️ **Funções Integradas aos Notebooks**

### **Cada notebook tem suas próprias funções:**

1. **Notebook 01**: `carregar_base_conhecimento()` - Para indexação no Pinecone
2. **Notebook 03**: `carregar_base_conhecimento_chains()` - Para uso com chains
3. **Todas**: Fallback automático se arquivo não existir

**✅ Vantagem:** Notebooks completamente autocontidos, sem dependências externas!

## 🎯 **Fluxo de Dados**

```
base_conhecimento.txt → Funções integradas nos Notebooks
                     ↓
            01-Pinecone indexa no vetor DB
                     ↓
         02-RAG busca semanticamente
                     ↓
        03-Chains processa por especialidade
                     ↓
        04-Router direciona automaticamente
                     ↓
         05-Sistema integra tudo
```

## 📝 **Como Adicionar Novos Dados**

1. **Edite apenas o arquivo `base_conhecimento.txt`**
2. **Siga o formato das seções:**

   ```txt
   ## ROTEIROS - [CIDADE]
   Nome: Descrição detalhada...

   ## LOGÍSTICA - [CIDADE]
   Nome: Descrição detalhada...
   ```

3. **Execute novamente os notebooks**
4. **Os dados serão atualizados automaticamente!**

## 🚀 **Resultado**

- ✅ **Código mais profissional**
- ✅ **Manutenção centralizada**
- ✅ **Dados consistentes**
- ✅ **Fácil expansão**
- ✅ **Separação código/dados**
- ✅ **Notebooks autocontidos**
- ✅ **Nenhum arquivo .py adicional**

---

🎉 **Sistema turístico limpo e profissional!**
