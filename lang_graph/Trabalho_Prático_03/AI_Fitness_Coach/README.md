# 🏋️‍♂️ **AI Fitness Coach**

> **Trabalho Prático - Redes Neurais Artificiais**

## 📓 **Aluno**

**AI Fitness Coach: Agente de Criação de Planilhas de Treino**  
**LangGraph + RAG + Cálculos Matemáticos para treinos personalizados**  
**Desenvolvido por: Kevin Siqueira Perdomo**  
**Matrícula: 201911250205**  
**Curso: Bacharelado em Engenharia De Computação**  
📧 **Email:** kevin.siqueira23@gmail.com  
🐙 **GitHub:** [Kevin-Perdomo](https://github.com/Kevin-Perdomo)

---> **Tecnologias:** LangGraph + RAG + Sentence-Transformers + ReportLab

---

## 🚀 Instalação

```bash
pip install -r requirements.txt
```

## ⚡ Execução

1. **Configure a API Key** (opcional):

   ```bash
   cp .env.example .env
   # Edite .env com sua chave Groq (se necessário)
   ```

2. **Execute o sistema completo** (VS Code recomendado):

   ```bash
   code 04-Sistema_Completo.ipynb
   ```

3. **Modifique seus dados** na célula 4:

   - Nome, idade, peso, altura
   - Periodicidade (2-6 dias/semana)
   - Objetivo: `hipertrofia`, `emagrecimento`, `força`, `condicionamento`
   - Experiência: `iniciante`, `intermediario`, `avancado`

4. **Execute todas as células** sequencialmente

## 📄 Saída

- **12 treinos únicos** organizados em 3 semanas
- **PDF personalizado** com cálculos de TMB, IMC e calorias
- **Progressão adaptada** ao seu objetivo

## 🏗️ Arquitetura LangGraph

![Fluxo LangGraph](fitness_langgraph.png)

**Pipeline de 4 nós:**

- **Validação**: Coleta e valida dados do usuário
- **Cálculos**: TMB, IMC, calorias e métricas personalizadas
- **Busca Info**: Sistema RAG + contexto especializado
- **Gera Treinos**: 12 treinos únicos adaptados ao perfil

## 📝 Funcionalidades

- ✅ Coleta e validação de dados
- ✅ Cálculos matemáticos (TMB, IMC, calorias)
- ✅ Sistema RAG com base de conhecimento fitness
- ✅ Geração de 12 treinos personalizados
- ✅ Exportação em PDF profissional

---
