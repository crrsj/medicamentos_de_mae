# 💊 Controle de Medicamentos

Painel web estático, responsivo e interativo para monitoramento diário de estoque de medicamentos por paciente. Desenvolvido com **HTML5**, **Tailwind CSS** e **JavaScript puro (Vanilla JS)**, utilizando um arquivo externo `dados.json` para o controle centralizado das informações.

---

## 🚀 Funcionalidades

- **Relógio em Tempo Real:** Exibição dinâmica da data e hora atual no cabeçalho do sistema.
- **Leitura via JSON:** Carregamento automático e independente dos dados de estoque e datas de atualização a partir de um arquivo externo `dados.json`.
- **Flags Visuais Automáticas de Estoque:**
  - 🟢 **Normal:** Quantidade $\ge 15$ unidades.
  - 🟡 **Alerta Amarelo:** Quantidade abaixo de 15 unidades ($< 15$).
  - 🔴 **Alerta Vermelho:** Quantidade abaixo de 10 unidades ($< 10$), com indicador pulsante.
- **Dashboard de Resumo:** Contadores dinâmicos do total de itens e alertas ativos.
- **Busca Interativa:** Filtro em tempo real por nome de paciente ou medicamento.

---

## 📂 Estrutura de Arquivos

```text
medicamentos/
│
├── index.html       # Página principal (Interface e Lógica JS)
├── dados.json       # Base de dados externa (Estoque, Pacientes e Datas)
└── README.md        # Documentação do projeto
```

---

## ⚙️ Como Executar o Projeto Localmente

Como a aplicação consome um arquivo externo (`dados.json`) via requisição assíncrona (`fetch`), o navegador exige a execução por meio de um servidor local para evitar bloqueios de segurança (CORS / Erro 404).

1. Abra a pasta do projeto no **VS Code**.
2. Certifique-se de clicar em **Trust** caso o editor solicite permissão de workspace.
3. Utilize a extensão **Live Server** (ou outro servidor web local de sua preferência).
4. Clique com o botão direito em `index.html` e selecione **"Open with Live Server"**.

---

## 📝 Como Atualizar os Dados

Para alterar as quantidades, descrições ou datas de atualização, edite diretamente o arquivo **`dados.json`** seguindo o formato padrão:

```json
[
    {
        "paciente": "Nome do Paciente",
        "medicamento": "Nome e Dosagem",
        "quantidade": 12,
        "dataAtualizacao": "09/10/2026 08:30",
        "descricao": "Instruções de uso ou observações."
    }
]
```

---

## 🌐 Hospedagem Sugerida

Para uso restrito ou publicação estática para poucos usuários, recomenda-se a utilização do **GitHub Pages** pela facilidade de deploy e gerenciamento de arquivos estáticos.