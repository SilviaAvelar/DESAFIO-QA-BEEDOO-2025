# Desafio QA Beedoo 2025 - Silvia Avelar

Este repositório contém toda a documentação e os artefatos gerados para o desafio de Analista de Qualidade de Software Júnior.
O objetivo foi realizar uma análise completa do módulo de "Desafio de perguntas e respostas Beedoo", documentando o processo desde a concepção da User Story até o reporte detalhado de bugs e sugestões de melhoria.

---

## 🚀 User Story Principal

**Como um administrador da plataforma, eu quero cadastrar um novo curso com nome e descrição, para que ele fique disponível na lista de cursos para os alunos.**

### Justificativa da User Story

A escolha desta User Story foi estratégica para analisar um fluxo de criação de dados, que é fundamental para a funcionalidade da plataforma.

*   **Perfil (Administrador):** Este é o usuário que alimenta o sistema com conteúdo. Sem a sua ação, a plataforma permaneceria vazia e sem valor para o usuário final (o aluno).
*   **Ação (Cadastrar um Curso):** Esta ação permite testar componentes essenciais como formulários, validação de campos e a persistência de dados, representando um cenário de teste rico e complexo.
*   **Valor para o Negócio:** A capacidade de adicionar novos cursos de forma eficiente é vital para o crescimento da plataforma. Uma falha neste processo representa um bloqueio direto à expansão do catálogo de produtos da empresa.

---

## 🛠️ Ferramentas Utilizadas

*   **GitHub:** Para versionamento e centralização da documentação do projeto.
*   **Google Sheets:** Para a criação e gerenciamento do plano de testes.
*   **Google Drive:** Para armazenamento e compartilhamento das evidências em vídeo (MP4).
*   **Screenpresso:** Para a captura das evidências de teste.

---

## 📂 Links para Artefatos de Teste

*   🔗 **[Plano de Testes Completo (Google Sheets)](https://docs.google.com/spreadsheets/d/1uOVeiClhhfAKRgEzCnHEjcGrri2S-zduXudNjvY_I4g/edit?usp=sharing)**: Contém todos os cenários e casos de teste em Gherkin.
*   📄 **[Relatório de Bugs Detalhado]([COLE AQUI O LINK PARA O SEU ARQUIVO RELATORIO_DE_BUGS.md])**: Documentação detalhada de todos os bugs e melhorias encontrados.
*   🎥 **[Pasta com Evidências em Vídeo (Google Drive)]([COLE AQUI O LINK PÚBLICO DA SUA PASTA NO DRIVE])**: Repositório com todos os vídeos de execução dos testes.

---

## ✨ Resumo de Sugestões de Melhoria

Durante a análise, foram identificadas oportunidades para melhorar a experiência do usuário (UX):

1.  **Carga Automática de Cursos:** A lista de cursos deveria carregar automaticamente na página inicial, sem a necessidade de um clique extra.
2.  **Cards de Cursos Interativos:** Os cards deveriam ser clicáveis, levando o usuário a uma página com detalhes completos sobre cada curso.


# Relatório de Bugs e Metodologia - Desafio QA Beedoo
**Autor:** Silvia Avelar
**Data:** 31/10/2025
**Aplicação Testada:** [Desafio de perguntas e respostas Beedoo](https://creative-sherbet-a51eac.netlify.app/)

Este documento detalha a metodologia de reporte de bugs utilizada e apresenta todos os achados (bugs funcionais e sugestões de melhoria) identificados durante a análise da aplicação.

---

## 1. Metodologia Utilizada: Relatório de Bug Padrão

Optei por utilizar uma metodologia de **Relatório de Bug Padrão**, focada em clareza, objetividade e reprodutibilidade.

### Justificativa da Escolha

Esta metodologia foi escolhida por ser universalmente compreendida por equipes de desenvolvimento, garantindo uma comunicação eficaz. O formato com "Passos para Reproduzir", "Resultado Esperado" e "Resultado Atual" permite que os desenvolvedores repliquem o erro de forma consistente, agilizando o processo de correção e alinhando-se com as práticas de metodologias ágeis.

---

## 2. Links para Artefatos de Teste

*   📄 **Documentação dos Casos de Teste (Google Sheets):**
    *   [Acessar Planilha de Casos de Teste](https://docs.google.com/spreadsheets/d/1uOVeiClhhfAKRgEzCnHEjcGrri2S-zduXudNjvY_I4g/edit?usp=sharing)

*   🎥 **Drive com Evidências em Vídeo (Google Drive):**
    *   [Acessar Pasta de Evidências](https://drive.google.com/drive/folders/12K7vOONMXHup8sTUYQoecTjzXgYWE5am?usp=sharing)

---

## 3. Lista de Bugs e Sugestões de Melhoria

### BUG-001: Função "Excluir Curso" Exibe Mensagem de Sucesso, Mas Não Remove o Curso
*   **Severidade:** Crítica
*   **Passos para Reproduzir:**
    1.  Cadastrar um curso na plataforma.
    2.  Na lista de cursos, clicar no botão "EXCLUIR CURSO".
*   **Resultado Esperado:** O sistema deveria exibir uma mensagem de sucesso E remover o curso da lista.
*   **Resultado Atual:** O sistema exibe a mensagem "Curso excluído com sucesso!", mas o curso permanece visível na lista. A função de exclusão não funciona.
*   **Evidência:** `[COLE AQUI O LINK PARA O VÍDEO ESPECÍFICO DESTE BUG]`

### BUG-002: Cadastro de curso é permitido com campos em branco
*   **Severidade:** Alta
*   **Passos para Reproduzir:**
    1.  Navegar para a página de cadastro de curso.
    2.  Não preencher nenhum dos campos do formulário.
    3.  Clicar em "CURSO CADASTRAR".
*   **Resultado Esperado:** O sistema deveria exibir mensagens de erro de validação e impedir o envio do formulário.
*   **Resultado Atual:** O sistema exibe a mensagem "Curso cadastrado com sucesso!", criando um registro inválido e vazio no sistema.
*   **Evidência:** `[COLE AQUI O LINK PARA O VÍDEO ESPECÍFICO DESTE BUG]`

### BUG-003: Desalinhamento Visual (Quebra de Layout) na Listagem de Cursos
*   **Severidade:** Média
*   **Passos para Reproduzir:**
    1.  Cadastrar três ou mais cursos.
    2.  Observar o alinhamento dos cards na página "Lista de cursos".
*   **Resultado Esperado:** Os cards dos cursos deveriam ser exibidos em uma grade organizada e alinhada.
*   **Resultado Atual:** Os cards são exibidos de forma desalinhada, com quebras de linha inconsistentes, criando um layout "quebrado".
*   **Evidência:** `[COLE AQUI O LINK PARA O SCREENSHOT OU VÍDEO DESTE BUG]`

### BUG-004: Funcionalidade "Listar Cursos" está inoperante
*   **Severidade:** Crítica
*   **Passos para Reproduzir:**
    1.  Acessar a aplicação pela primeira vez.
    2.  Clicar no botão "LISTAR CURSOS" no cabeçalho.
*   **Resultado Esperado:** A lista de cursos deveria ser recarregada ou atualizada.
*   **Resultado Atual:** O botão não executa nenhuma ação visível.
*   **Evidência:** `[COLE AQUI O LINK PARA O VÍDEO ESPECÍFICO DESTE BUG]`

### MELHORIA-001: Carga automática de cursos e redundância na interface
*   **Tipo:** Sugestão de Usabilidade (UX)
*   **Descrição:** A página inicial já se intitula "Lista de cursos", mas exige que o usuário clique em um botão para carregar o conteúdo, o que é redundante e confuso.
*   **Sugestão:** A lista de cursos deve ser carregada automaticamente ao acessar a página. O botão "LISTAR CURSOS" no cabeçalho pode ser removido para simplificar a interface.

### MELHORIA-002: Cards de Cursos Não São Interativos (Não Clicáveis)
*   **Tipo:** Sugestão de Usabilidade (UX)
*   **Descrição:** O usuário não pode clicar nos cards para ver mais detalhes sobre um curso, limitando a interação a uma visualização superficial.
*   **Sugestão:** Transformar cada card em um link para uma página de "Detalhes do Curso", exibindo todas as informações cadastradas.
