# 📅 Seleção de Bases - EMI Eventos (IFB)

Sistema web desenvolvido para o **Instituto Federal de Brasília (IFB)** para gerenciar a seleção de bases práticas das estudantes do curso **Ensino Médio Integrado em Eventos**.

O sistema permite que as estudantes escolham suas bases em tempo real, respeitando o limite de vagas por ano (1º, 2º e 3º ano) e evitando conflitos de horários.

## 🚀 Funcionalidades

### 👩‍🎓 Para Estudantes
- **Login Simplificado:** Acesso via número de matrícula.
- **Visualização em Tempo Real:** Vagas atualizadas instantaneamente (sem precisar recarregar a página).
- **Regras de Negócio:**
  - Bloqueio automático quando a base lota.
  - Bloqueio de vagas específicas por ano (Cotas).
  - Impede duplicidade (uma estudante não pode ocupar duas bases).
- **Feedback Visual:** Confirmação imediata da inscrição.

### 🔐 Para Coordenação (Admin)
- **Painel Administrativo:** Acesso protegido por senha.
- **Monitoramento:** Visualização da lista de inscritos em tempo real.
- **Filtros:** Visualizar por base específica.
- **Gestão:** Possibilidade de remover uma inscrição manualmente.
- **Backup:** Exportação dos dados para Excel (.CSV).
- **Reset:** Função de segurança para zerar o sistema (protegida por senha secundária).

---

## 🛠️ Tecnologias Utilizadas

- **Frontend:** HTML5, CSS3 (Responsivo), JavaScript (ES6 Modules).
- **Backend/Database:** Google Firebase Realtime Database.
- **Hospedagem:** GitHub Pages.

---

## 📂 Estrutura do Projeto

O projeto foi refatorado para facilitar a manutenção dos dados sem mexer na lógica do sistema:

- `index.html`: Contém toda a estrutura visual (HTML), estilos (CSS) e a lógica de conexão com o Firebase.
- `dados.js`: Arquivo dedicado apenas para os dados que mudam anualmente.
  - Lista de Estudantes (`DATABASE_ALUNAS`)
  - Configuração das Bases (`BASES_CONFIG`)
  - Regras de Cotas (`COTAS`)
- `logo-ifb.png`: Identidade visual do campus.

---

## ⚙️ Como Configurar/Atualizar

### Para mudar a lista de estudantes:
1. Abra o arquivo `dados.js`.
2. Atualize a constante `DATABASE_ALUNAS` com os novos dados (Matrícula, Nome e Ano).
3. Salve e suba para o GitHub.

### Para iniciar um novo processo seletivo:
1. Acesse o Painel da Coordenação.
2. Clique em "Resetar Sistema".
3. Digite a senha de segurança (definida no código como `RESET_PASSWORD`).
   * *Isso apagará todos os dados do Firebase, deixando o sistema pronto para novas inscrições.*

---

## 🖥️ Como Rodar Localmente

Como o projeto utiliza **Módulos JavaScript** (`type="module"`) e importação de arquivos externos, ele não funciona se abrir direto pelo arquivo (clicar duas vezes no `index.html`).

Para testar no seu computador:
1. Instale uma extensão como **"Live Server"** no VS Code.
2. Ou use python no terminal: `python -m http.server`.
3. Ou simplesmente suba para o GitHub Pages, que já configura o ambiente corretamente.

---

<div align="center">
  Feito com 💗 pelas docentes do EMI em Eventos | IFB Brasília
</div>
