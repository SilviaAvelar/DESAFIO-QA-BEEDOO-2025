# Relatório de Bugs e Sugestões de Melhoria
**Aplicação Testada:** [Desafio de perguntas e respostas Beedoo](https://creative-sherbet-a51eac.netlify.app/)

Este documento apresenta a lista detalhada de todos os bugs funcionais e sugestões de melhoria de usabilidade (UX) identificados durante a fase de testes.

---

### BUG-001: Função "Excluir Curso" Exibe Mensagem de Sucesso, Mas Não Remove o Curso
*   **Severidade:** Crítica  

**Passos para Reproduzir:**
1. Cadastrar um curso na plataforma.
2. Na lista de cursos, clicar no botão "EXCLUIR CURSO".
   
*   **Resultado Esperado:** O sistema deveria exibir uma mensagem de sucesso E remover o curso da lista.
*   **Resultado Atual:** O sistema exibe a mensagem "Curso excluído com sucesso!", mas o curso permanece visível na lista.
*   **Evidência:** [Ver Evidência em Vídeo](https://drive.google.com/file/d/1M_LWeDS6lwGUaav93ep9xnb-WBei0F3E/view?usp=sharing)

### BUG-002: Cadastro de curso é permitido com todos os campos em branco
*   **Severidade:** Alta

**Passos para Reproduzir:**
1. Navegar para a página de cadastro de curso.
2. Não preencher nenhum dos campos do formulário.
3. Clicar em "CURSO CADASTRAR".

*   **Resultado Esperado:** O sistema deveria exibir mensagens de erro de validação e impedir o envio do formulário.
*   **Resultado Atual:** O sistema exibe a mensagem "Curso cadastrado com sucesso!", criando um registro inválido.
*   **Evidência:** [Ver Evidência em Vídeo](https://drive.google.com/file/d/1nXsP_rDX98SwsVSDzufrYpJRGXOeJ9FH/view?usp=sharing)

### BUG-003: Desalinhamento Visual (Quebra de Layout) na Listagem de Cursos
*   **Severidade:** Média
  
**Passos para Reproduzir:**
1. Cadastrar três ou mais cursos.
2. Observar o alinhamento dos cards na página "Lista de cursos".
   
*   **Resultado Esperado:** Os cards dos cursos deveriam estar alinhados em uma grade organizada.
*   **Resultado Atual:** Os cards são exibidos de forma desalinhada, com quebras de linha inconsistentes.
*   **Evidência:** [Ver Evidência em Vídeo](https://drive.google.com/file/d/1R-13CMdG8BAMCpHcxGCV26n6OXIBem4n/view?usp=sharing)
  
---

---

### Sugestões de Melhoria (UX e Funcionalidades)

### MELHORIA-001: Implementar Gerenciamento de Cursos (Edição e Exclusão Funcional)
*   **Descrição:** Atualmente, a aplicação não oferece nenhuma forma funcional de gerenciar os cursos após a criação. Não há funcionalidade de edição para corrigir erros ou atualizar informações. Além disso, a função de exclusão existente está quebrada (conforme documentado no BUG-001), deixando o usuário sem nenhuma opção para corrigir ou remover um curso cadastrado.
*   **Sugestão:**
    1.  **Priorizar a Correção da Exclusão:** Corrigir o `BUG-001` para que a funcionalidade de excluir funcione conforme o esperado.
    2.  **Implementar a Edição (Update):** Adicionar um botão "Editar" em cada card de curso, que levaria a um formulário pré-preenchido, permitindo a atualização dos dados. Isso completaria as operações básicas de um CRUD (Create, Read, **Update**, **Delete**).

### MELHORIA-002: Implementar Confirmação Antes de Excluir
*   **Descrição:** A exclusão de um curso é uma ação destrutiva e imediata. Um clique acidental pode levar à perda de dados permanentemente.
*   **Sugestão:** Implementar uma janela de confirmação (modal) que pergunte "Você tem certeza que deseja excluir este curso?" antes de a ação ser executada.

### MELHORIA-003: Adicionar Barra de Busca e Filtros
*   **Descrição:** Conforme a lista de cursos cresce, encontrar um curso específico se torna uma tarefa manual e demorada.
*   **Sugestão:** Adicionar uma barra de busca para pesquisar cursos por nome e opções de filtro (ex: por "Tipo de curso" - Online/Presencial).

### MELHORIA-004: Cards de Cursos Não São Interativos (Não Clicáveis)
*   **Descrição:** O usuário não pode clicar nos cards para ver mais detalhes sobre um curso, limitando a interação.
*   **Sugestão:** Transformar cada card em um link para uma página de "Detalhes do Curso".
