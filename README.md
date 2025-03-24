# 🔄 Revolução de Linha de Produção

<p align="center">
  <img src="https://img.shields.io/badge/STATUS-EM%20DESENVOLVIMENTO-yellowgreen" alt="Status">
  <img src="https://img.shields.io/github/last-commit/xygabp/Revolucao-da-Gestao-de-Linha-de-Producao?color=blue" alt="Último commit">
</p>

**Software de Otimização de Alocação Industrial**  
*Projeto de Engenharia de Software II - PUCRS*  

---

## 📌 Visão do Projeto
Solução inteligente para gestão de recursos humanos em ambientes industriais que:

- **Alocação Dinâmica**  
  Utiliza algoritmos de otimização para distribuir colaboradores conforme suas competências técnicas e demandas de produção, reduzindo tempo ocioso em 30-40%.

- **Monitoramento Visual**  
  Interface gráfica interativa que representa a linha de produção em formato oval, com cores que indicam em tempo real:
  - 🟢 Postos operando com eficiência ideal  
  - 🟡 Postos com desempenho aceitável  
  - 🔴 Gargalos críticos que exigem intervenção

- **Gestão de Competências**  
  Sistema integrado de job rotation que:
  1. Mapeia habilidades por colaborador
  2. Sugere treinamentos cruzados
  3. Acompanha progresso em novos postos

---

## 📂 Documentação Técnica

### 👥 Perfis de Personas
Análise detalhada dos principais usuários do sistema:

| Tipo          | Necessidades Primárias                  | Dificuldades Comuns               |
|---------------|-----------------------------------------|-----------------------------------|
| **Gestor**    | Visão macro da produção                 | Identificar gargalos rapidamente  |
| **Supervisor**| Alocação diária de equipes              | Balancear habilidades x demanda   |
| **Operador**  | Clareza nas tarefas diárias             | Reportar problemas de produção    |

[🔗 Acesse documento completo de Personas](https://docs.google.com/document/d/1YHtOTNKCfL13RduCq9Js9xZ82KgPFtei/edit?usp=sharing)

### 💰 Modelo de Monetização
Estratégia de negócios com projeção financeira para 3 anos:

- **Mercado-Alvo**: Indústrias de médio/grande porte
- **Modelo Principal**: SaaS (assinaturas mensais)
- **Planos**:  
  - Básico (R$ 500/mês): 1 linha de produção  
  - Premium (R$ 2.000/mês): Linhas ilimitadas + relatórios avançados

[🔗 Acesse plano financeiro detalhado](https://docs.google.com/document/d/1XBHqTbrBoD-VlA464C1OhgyH3wV5qKvn/edit?usp=sharing)

---

## 🛠️ Arquitetura do Sistema
<div align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original-wordmark.svg" width="80" title="Backend Java"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original-wordmark.svg" width="80" title="Spring Framework"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original-wordmark.svg" width="80" title="Banco de Dados MySQL"/>
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original-wordmark.svg" width="80" title="Frontend Bootstrap"/>
</div>

### Camadas Principais:
1. **Frontend**  
   - Bootstrap 5 + Thymeleaf para templates dinâmicos
   - Konva.js para visualização interativa do layout fabril

2. **Backend**  
   - Java 17 com Spring Boot 3.2
   - Algoritmos de programação linear para otimização

3. **Dados**  
   - MySQL 8.0 com modelagem relacional
   - Armazena histórico de produção por operador

---

## 🚀 Guia de Implementação

### Pré-requisitos
- Java Development Kit 17+
- MySQL Server 8.0+
- Maven 3.8+

### Passo a Passo
```bash
# 1. Clonar repositório
git clone https://github.com/xygabp/Revolucao-da-Gestao-de-Linha-de-Producao.git

# 2. Configurar banco de dados (execute no MySQL)
CREATE DATABASE producao_db;
CREATE USER 'prod_user'@'localhost' IDENTIFIED BY 'senha_segura';
GRANT ALL PRIVILEGES ON producao_db.* TO 'prod_user'@'localhost';

# 3. Iniciar aplicação
cd Revolucao-da-Gestao-de-Linha-de-Producao
./mvnw spring-boot:run
