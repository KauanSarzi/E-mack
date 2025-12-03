
# 📊 E-Mack - Sistema de Análise de Dados de E-commerce

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Data Analysis](https://img.shields.io/badge/Analysis-E--commerce-green.svg)]()
[![HTML Reports](https://img.shields.io/badge/Reports-HTML-orange.svg)]()

> **Sistema de análise de dados para e-commerce com geração automatizada de relatórios HTML, desenvolvido para processamento e visualização de métricas de produtos e vendas.**

---

## 📋 Índice

- [Sobre o Projeto](#-sobre-o-projeto)
- [Funcionalidades](#-funcionalidades)
- [Demonstração](#-demonstração)
- [Tecnologias Utilizadas](#-tecnologias-utilizadas)
- [Estrutura do Projeto](#-estrutura-do-projeto)
- [Como Executar](#-como-executar)
- [Casos de Uso](#-casos-de-uso)
- [Exemplos de Saída](#-exemplos-de-saída)
- [Aprendizados e Desafios](#-aprendizados-e-desafios)
- [Melhorias Futuras](#-melhorias-futuras)
- [Autor](#-autor)

---

## 🎯 Sobre o Projeto

**E-Mack** é um sistema de análise de dados desenvolvido em Python para processar informações de produtos de e-commerce. O projeto foi criado como parte das atividades acadêmicas da disciplina de Programação, demonstrando competências em:

- **Manipulação de dados estruturados** (CSV)
- **Algoritmos de ordenação e filtragem**
- **Geração dinâmica de relatórios HTML**
- **Estruturação de código modular**

### Problema Abordado

Empresas de e-commerce precisam analisar grandes volumes de dados de produtos para:
- ❌ Identificar produtos mais vendidos por categoria
- ❌ Calcular proporções de best-sellers
- ❌ Visualizar distribuição de preços
- ❌ Gerar relatórios executivos rapidamente

### Solução Implementada

O E-Mack automatiza essas análises através de:
- ✅ **6 módulos de análise** diferentes
- ✅ **Relatórios HTML responsivos** com CSS integrado
- ✅ **Interface CLI interativa** para seleção de análises
- ✅ **Processamento eficiente** de datasets com 800+ produtos

---

## 🚀 Funcionalidades

### 1. **Contagem de Produtos por Categoria**
Analisa o dataset e retorna o número total de produtos em cada categoria (Livros, Casa, Esportes, Eletrônicos, Moda).

### 2. **Percentual de Produtos por Categoria**
Calcula e exibe a distribuição percentual de produtos entre as categorias disponíveis.

### 3. **Análise de Best-Sellers**
Identifica a proporção de produtos best-sellers em cada categoria, permitindo análise de desempenho comercial.

### 4. **Ranking de Preços**
Gera listagem dos 10 produtos mais caros e mais baratos do catálogo, útil para estratégias de precificação.

### 5. **Listagem por Categoria Escolhida**
Permite ao usuário selecionar uma categoria e gera relatório HTML com todos os produtos daquela categoria.

### 6. **Relatório Top 10 Best-Sellers por Categoria**
Cria documento HTML completo com os 10 produtos mais vendidos em cada categoria, ordenados por volume de vendas do último mês.

---

## 🎨 Demonstração

### Interface do Menu
```
1- Contagem de produtos por categoria
2- Percentual de produtos por categoria
3- Avaliar a proporção de produtos best-sellers em cada categoria
4- Identificar os 10 produtos mais caros e mais baratos no geral
5- Listar os produtos por categoria escolhida
6- Gerar um relatório em HTML demonstrando os Top 10 bestsellers por categoria
```

### Exemplo de Saída - Análise de Best-Sellers
```
Livros: 54.2 %
Casa: 48.7 %
Esporte: 51.3 %
Eletrônicos: 49.8 %
Moda: 52.1 %
```

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Propósito |
|------------|-----------|
| **Python 3.8+** | Linguagem principal do projeto |
| **CSV** | Formato de armazenamento de dados |
| **HTML5 + CSS3** | Geração de relatórios visuais |
| **Algoritmos de Ordenação** | Processamento e ranking de dados |

### Estruturas de Dados
- **Listas**: Armazenamento de dataset e resultados
- **Dicionários**: Representação de produtos individuais
- **List Comprehension**: Cálculos eficientes de proporções

---

## 📁 Estrutura do Projeto

```
emack-analysis/
├── gerar_relatorio_html.py      # Script principal
├── emack.csv                     # Dataset de produtos (800+ registros)
└── README.md                     # Documentação
```

### Arquitetura do Código

```python
# Módulo de Carregamento
carregar_dados()              # Lê CSV e converte para estrutura Python

# Módulos de Análise
listarCategorias()            # Extrai categorias únicas
cont_produtos_categoria()     # Contabiliza produtos
percentCategoria()            # Calcula distribuições
best_sallers_categoria()      # Analisa best-sellers

# Módulos de Ranking
top10_caros()                 # Ordena por preço (DESC)
top10_baratos()               # Ordena por preço (ASC)

# Módulos de Geração de Relatórios
gerarHtml_BestSellers()       # Relatório HTML completo
gerarHtml_ProdutosPorCategoria()  # Relatório por categoria
```

---

## 🚀 Como Executar

### Pré-requisitos
- Python 3.8 ou superior instalado
- Arquivo `emack.csv` no mesmo diretório do script

### Passos

1. **Clone o repositório**
```bash
git clone https://github.com/seu-usuario/E-mack.git
cd E-mack
```

2. **Verifique os arquivos**
```bash
ls
# Deve listar: gerar_relatorio_html.py, emack.csv
```

3. **Execute o programa**
```bash
python gerar_relatorio_html.py
```

4. **Interaja com o menu**
```
Digite o número da opção desejada (1-6)
Para sair, digite 7
```

5. **Acesse os relatórios gerados**
```bash
# Abra os arquivos HTML no navegador
open relatorio_top_10_best_sellers.html
```

---

## 💼 Casos de Uso

### 1. Análise de Portfólio
**Cenário**: Gerente de produto precisa entender a distribuição do catálogo.

**Solução**: Opções 1 e 2 fornecem visão quantitativa e percentual da distribuição de produtos.

### 2. Estratégia de Marketing
**Cenário**: Time de marketing quer focar nas categorias com mais best-sellers.

**Solução**: Opção 3 identifica categorias com maior proporção de produtos de destaque.

### 3. Precificação Competitiva
**Cenário**: Analista de pricing precisa ajustar preços do catálogo.

**Solução**: Opção 4 lista produtos nos extremos da tabela de preços para benchmarking.

### 4. Relatórios Executivos
**Cenário**: Apresentação para stakeholders sobre top performers.

**Solução**: Opção 6 gera relatório HTML profissional com top 10 por categoria.

---

## 📊 Exemplos de Saída

### Relatório HTML - Top 10 Best-Sellers

```html
<html>
<head>
    <title>Relatório Top 10 Best Sellers por Categoria</title>
</head>
<body>
    <h1>Eletrônicos</h1>
    <ol>
        <li>Produto 73 - Quantidade Vendida: 9599</li>
        <li>Produto 55 - Quantidade Vendida: 9572</li>
        <li>Produto 34 - Quantidade Vendida: 9550</li>
        <!-- ... -->
    </ol>
    <!-- Outras categorias -->
</body>
</html>
```

### Console - Análise de Percentual

```
Livros: 20.125 %
Casa: 19.875 %
Esporte: 20.25 %
Eletrônicos: 19.625 %
Moda: 20.125 %
```

---

## 🎓 Aprendizados e Desafios

### Competências Desenvolvidas

#### 1. **Manipulação de Arquivos**
- Leitura e parsing de CSV
- Tratamento de encoding de caracteres especiais
- Geração dinâmica de arquivos HTML

#### 2. **Algoritmos e Estruturas de Dados**
- Implementação de ordenação com `sorted()` e `key functions`
- Uso de list comprehension para cálculos eficientes
- Manipulação de dicionários aninhados

#### 3. **Boas Práticas de Código**
- Modularização de funcionalidades
- Nomenclatura descritiva de variáveis
- Separação de lógica de apresentação

### Desafios Superados

| Desafio | Solução Implementada |
|---------|---------------------|
| **Ordenação complexa** | Uso de funções `key` customizadas (ex: `preco_produto()`) |
| **Filtragem por categoria** | Função `listarProdutosCategoria()` com comparação de strings |
| **Geração de HTML dinâmico** | Concatenação de strings com f-strings e loops |
| **Interface de seleção** | Menu interativo com validação de entrada |

---

## 🔮 Melhorias Futuras

### Fase 1: Visualização de Dados 📈
- [ ] Integração com Matplotlib para gráficos de barras
- [ ] Gráficos de pizza para distribuição de categorias
- [ ] Dashboard interativo com Plotly

### Fase 2: Análises Avançadas 🔍
- [ ] Correlação entre preço e volume de vendas
- [ ] Análise temporal (se houver dados de data)
- [ ] Detecção de outliers em preços
- [ ] Recomendação de produtos baseada em padrões

### Fase 3: Interface Web 🌐
- [ ] Conversão para aplicação Flask/Django
- [ ] Upload de CSV via interface web
- [ ] Download de relatórios em PDF
- [ ] Sistema de autenticação para múltiplos usuários

### Fase 4: Performance e Escalabilidade ⚡
- [ ] Uso de Pandas para datasets maiores
- [ ] Cache de resultados frequentes
- [ ] Processamento paralelo para grandes volumes
- [ ] Conexão com banco de dados (PostgreSQL/MySQL)

---

## 👨‍💻 Autor

**Kauan Sarzi da Rocha**
- Matrícula: 10427235
- Turma: 01J
- Instituição: [Universidade Presbiteriana Mackenzie]
- Curso: Sistemas de Informação

### 📫 Contato
- LinkedIn: [linkedin.com/in/kauan-sarzi](https://linkedin.com/in/kauan-sarzi)
- GitHub: [github.com/kauansarzi](https://github.com/KauanSarzi)
- E-mail: kauansarzi24@gmail.com

---

## 📄 Licença

Este projeto foi desenvolvido para fins acadêmicos. Sinta-se livre para utilizar o código como referência para estudos, citando o autor original.

---



<div align="center">

**⭐ Se este projeto foi útil para você, considere dar uma estrela no repositório!**


</div>
