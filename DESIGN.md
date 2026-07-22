# Documento de Design de Sistema (Visão da Interface)

## Projeto

**eBook IA + n8n do Zero**

Objetivo: criar uma interface limpa, intuitiva e fácil de usar para quem nunca teve contato com IA ou n8n.

---

# Conceito Visual

O visual deve transmitir simplicidade, organização e tecnologia, sem parecer complicado.

Inspirado em plataformas como:

* Notion
* GitBook
* Documentação do n8n
* Documentação da OpenAI

O foco é facilitar a leitura e a navegação.

---

# Estrutura da Tela Inicial

```text
+------------------------------------------------------+
| Logo                     IA + n8n do Zero            |
|------------------------------------------------------|
| Início | Capítulos | Projetos | Recursos | Sobre     |
|------------------------------------------------------|
|                                                      |
|      IA + n8n do Zero                                |
|                                                      |
| Aprenda Inteligência Artificial e Automações         |
| do zero, com exemplos práticos.                      |
|                                                      |
| [ Começar Agora ]                                    |
|                                                      |
|------------------------------------------------------|
| Últimos capítulos                                    |
|                                                      |
| 📘 Introdução                                        |
| 📘 O que é IA                                        |
| 📘 O que é n8n                                       |
| 📘 Primeiro Workflow                                 |
|                                                      |
|------------------------------------------------------|
| Rodapé                                               |
+------------------------------------------------------+
```

---

# Cabeçalho

O usuário vê:

* Logo do projeto.
* Nome do eBook.
* Menu de navegação.

Botões disponíveis:

* Início
* Capítulos
* Projetos
* Recursos
* Sobre

---

# Botão "Início"

### Quando o usuário clicar:

1. A página volta ao topo.
2. A capa do eBook aparece.
3. O texto de apresentação é exibido.
4. O botão "Começar Agora" fica visível.

Objetivo: levar rapidamente o leitor ao início da experiência.

---

# Botão "Capítulos"

Ao clicar:

1. A lista completa dos capítulos é exibida.
2. Cada capítulo mostra:

   * número;
   * título;
   * breve descrição;
   * tempo estimado de leitura.

Exemplo:

```text
Capítulo 1

O que é Inteligência Artificial

★★★★★

Leitura: 8 minutos

[ Ler ]
```

---

# Botão "Ler"

Quando clicar:

1. O capítulo é aberto.
2. A barra lateral destaca o capítulo atual.
3. O texto aparece formatado.
4. As imagens são exibidas ao longo da leitura.
5. Ao final, aparecem exercícios e um botão para avançar.

---

# Botão "Próximo"

Ao clicar:

1. O sistema salva automaticamente o progresso (LocalStorage).
2. O próximo capítulo é carregado.
3. A barra de progresso é atualizada.
4. O topo do novo capítulo é exibido.

---

# Botão "Anterior"

Quando pressionado:

1. O capítulo anterior é aberto.
2. A posição volta ao início da página.
3. O progresso permanece salvo.

---

# Botão "Projetos"

Esta seção reúne exemplos práticos.

Cada projeto é apresentado como um cartão:

```text
Projeto 01

Responder e-mails com IA

★★★★★

Tempo:
15 minutos

[Demonstração]

[Passo a Passo]
```

---

# Botão "Demonstração"

Ao clicar:

1. Uma explicação do projeto é exibida.
2. Um diagrama simples mostra o fluxo da automação.
3. O usuário entende o objetivo antes de começar.

---

# Botão "Passo a Passo"

Quando clicado:

O sistema apresenta:

1. Objetivo do projeto.
2. Ferramentas necessárias.
3. Configuração inicial.
4. Construção do workflow.
5. Testes.
6. Resultado esperado.

---

# Botão "Recursos"

Exibe uma lista de materiais complementares, como:

* Glossário de termos.
* Prompts prontos.
* Templates de workflows.
* Lista de ferramentas recomendadas.
* Checklist de estudos.

Cada recurso possui um botão de acesso ou download.

---

# Botão "Sobre"

Mostra:

* propósito do eBook;
* para quem foi criado;
* objetivos de aprendizado;
* versão do material;
* formas de contato (se desejado).

---

# Barra de Progresso

Durante a leitura existe uma barra horizontal indicando quanto do capítulo foi percorrido.

Exemplo:

```text
██████████░░░░░░░░░░░

45%
```

Ela aumenta conforme o usuário rola a página.

---

# Barra Lateral

Enquanto lê um capítulo, o usuário vê uma navegação lateral:

```text
Capítulos

✔ Introdução

✔ O que é IA

► O que é n8n

○ Primeiro Workflow

○ APIs

○ Agentes

○ Projetos
```

Isso facilita saber onde está e acessar qualquer seção rapidamente.

---

# Rodapé

No final de cada página ficam disponíveis:

* botão **Anterior**;
* botão **Próximo**;
* link para voltar ao topo;
* indicação da versão do eBook.

---

# Fluxo Principal do Usuário

```text
Acessa o site
      │
      ▼
Tela inicial
      │
      ▼
Clica em "Começar Agora"
      │
      ▼
Lista de capítulos
      │
      ▼
Escolhe um capítulo
      │
      ▼
Lê o conteúdo
      │
      ▼
Faz os exercícios
      │
      ▼
Clica em "Próximo"
      │
      ▼
Avança para o capítulo seguinte
      │
      ▼
Conclui todos os módulos
      │
      ▼
Explora os projetos práticos
      │
      ▼
Baixa recursos complementares
      │
      ▼
Finaliza o eBook
```

## Princípios de Design

* **Poucos botões por tela:** evita sobrecarregar iniciantes.
* **Leitura confortável:** tipografia grande, bom espaçamento e contraste adequado.
* **Navegação consistente:** os mesmos elementos aparecem em todas as páginas.
* **Feedback imediato:** ao clicar em um botão, o usuário percebe claramente o resultado (mudança de página, destaque do capítulo, atualização da barra de progresso ou confirmação de download).
* **Escalabilidade:** novos capítulos, projetos e recursos podem ser adicionados sem alterar a estrutura principal da interface.
