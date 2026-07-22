# ADR (Architecture Decision Record)

## Projeto

**eBook "IA + n8n do Zero"**

**ADR Nº:** 001
**Status:** Aprovado
**Data:** 21/07/2026

---

# Título

Escolha de uma arquitetura simples, gratuita e sem necessidade de programação avançada.

---

# Contexto

O projeto consiste em criar um eBook digital sobre Inteligência Artificial e n8n para iniciantes.

Os objetivos principais são:

* ser simples de construir;
* funcionar em qualquer navegador;
* não depender de servidores;
* não gerar custos;
* ser fácil de atualizar;
* permitir publicação gratuita.

Como o produto é um eBook (e pode futuramente evoluir para uma versão interativa), não há necessidade de uma arquitetura complexa, banco de dados ou frameworks pesados.

---

# Decisão

Foi escolhida a seguinte arquitetura:

* **HTML5** para estruturar o conteúdo.
* **CSS3** para o visual.
* **JavaScript (Vanilla JS)** para pequenas interações.
* **Arquivos Markdown (.md)** para escrever e organizar o conteúdo dos capítulos.
* **Git + GitHub** para controle de versão.
* **GitHub Pages** para publicar gratuitamente.
* **Visual Studio Code** como editor.

Toda a aplicação será estática.

Não haverá servidor, banco de dados ou backend.

---

# Arquitetura

```text
Usuário
   │
   ▼
Navegador
   │
   ▼
HTML
 │
 ├── CSS
 │
 ├── JavaScript
 │
 ├── Imagens
 │
 └── Conteúdo (Markdown/HTML)
```

---

# Estrutura de Pastas

```text
ebook-ia-n8n/

│
├── index.html
├── sobre.html
├── capitulos.html
├── contato.html
│
├── css/
│      style.css
│
├── js/
│      script.js
│
├── img/
│      capa.png
│      icones/
│
├── capitulos/
│      01-introducao.md
│      02-ia.md
│      03-n8n.md
│      ...
│
└── README.md
```

---

# Tecnologias Escolhidas

| Tecnologia   | Motivo                        |
| ------------ | ----------------------------- |
| HTML         | Estrutura das páginas         |
| CSS          | Estilo visual                 |
| JavaScript   | Interações leves              |
| Markdown     | Escrita simples dos capítulos |
| Git          | Controle de versões           |
| GitHub       | Hospedagem do código          |
| GitHub Pages | Publicação gratuita           |
| VS Code      | Editor gratuito               |

---

# O que NÃO será utilizado

Para manter o projeto simples, **não serão utilizados**:

* React
* Angular
* Vue
* Next.js
* Node.js
* PHP
* Laravel
* Banco de Dados
* Firebase
* Supabase
* Docker
* Kubernetes
* APIs obrigatórias
* Serviços pagos

Essas tecnologias podem ser consideradas em uma evolução futura, mas não são necessárias para entregar valor na primeira versão.

---

# Vantagens

* **100% gratuito**.
* Funciona offline (após carregado).
* Hospedagem gratuita.
* Fácil manutenção.
* Curva de aprendizado baixa.
* Excelente desempenho.
* Compatível com computadores e celulares.
* Conteúdo organizado e versionado.

---

# Desvantagens

* Não possui autenticação de usuários.
* Não salva progresso de leitura entre dispositivos.
* Não oferece funcionalidades online avançadas.
* Recursos interativos mais sofisticados exigiriam JavaScript adicional.

Para um eBook, essas limitações não comprometem a proposta inicial.

---

# Evolução Futura (Opcional)

Caso o projeto cresça, será possível adicionar gradualmente:

* Busca por palavras-chave.
* Modo escuro.
* Marcação de capítulos concluídos (LocalStorage).
* Sistema de favoritos.
* Quiz ao final dos capítulos.
* Barra de progresso da leitura.
* Download de materiais extras.
* Área de membros.
* Integração com IA para perguntas sobre o conteúdo.
* Templates de workflows do n8n para download.
