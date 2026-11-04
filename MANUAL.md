# 🍋 SmartPOS Manual (English)
Complete guide: how to open, create your login and password, make sales, control the cash register, register products, and keep everything secure.

## Index
1. What's in the package
2. How to open the program
3. First access: create login and password
4. Sign in, sign out, and lock screen
5. Users: Manager and Cashier
6. Daily routine: opening the register
7. Making a sale
8. Cash in, cash out, and closing the register
9. Products and inventory
10. Promotions
11. History, cancellation, and reports
12. Settings and backup
13. Security and audit
14. Keyboard shortcuts
15. Common issues
16. For developers

---

## 1. What's in the package
| File | Purpose |
| :--- | :--- |
| `index.html` | The program. A single file, no installation and no internet required. |
| `MANUAL.md` | This manual. |
| `README.md` | Technical project summary (same as on GitHub). |

---

## 2. How to open the program
1. Extract the ZIP: right-click the file → Extract all...
2. Place the folder in a fixed location, e.g., `Documents\POS`. Do not move the file afterwards.
3. Double-click `index.html`. It will open in your web browser.
4. Always use the same browser (updated Chrome, Edge, or Brave).

💡 **Tip:** Drag the file to your bookmarks bar, or create a shortcut on your desktop, to open it quickly every day.

**Where is the data stored?** Products, sales, cash registers, and users are stored inside the browser of this computer, not in the file itself. Therefore:
- Opening it in another browser or on another computer will show an empty system.
- Clearing browsing data/cookies in the browser will erase everything.
- **Make backups weekly.**

---

## 3. First access: create login and password
The system does not come with a default user or password. The first time you open it, it displays the "Welcome!" screen for you to create the Manager account (the system owner).

1. **Store name:** Appears at the top and on the receipt.
2. **Your name:** E.g., "João Resende".
3. **Username:** What you type to sign in. Use only lowercase letters, numbers, dots, hyphens, or underscores, 3 to 32 characters long. Examples: `joao`, `maria.silva`.
4. **Password:** At least 8 characters, containing letters and numbers. The colored bar shows password strength.
   * Cannot contain your username or be an obvious password (like `12345678` or `password123`).
   * Strong password example: mix uppercase, lowercase, numbers, and symbols, e.g., `SmartPOS#2026` (create your own!).
5. Repeat the password in **Confirm password** and click **Create account and sign in**.

⚠️ **VERY IMPORTANT: Recovery Code.** Right after creating the account, a code like this appears: `ABCD-EFGH-JKLM-NPQR`.
- Write it down on paper and store it in a safe place.
- It is the only way to recover access if the manager forgets the password.
- It will not be shown again. If you lose it, generate a new one in **Security** while you still remember your password.

---

## 4. Sign in, sign out, and lock screen

### Sign in
Type your username and password and click **Sign in**. The 👁 icon next to the password reveals what you typed. If "Caps Lock is on" appears, turn off your Caps Lock key.

### Sign out
In the bottom left corner, next to your name, click the logout icon (arrow pointing out). On mobile, it is located at the top.

### Lock screen (quick pause)
Click the padlock icon at the top or press `Ctrl + Shift + L`. To return, simply type your password, and your cart will be right where you left it.
The screen also locks automatically after 10 minutes of inactivity. This time can be changed in **Security**.

### Typed the wrong password too many times?
After 5 incorrect attempts, the account is locked for 5 minutes. If you fail again, the time doubles (10, 20, 40 mins..., up to 1 hour). This prevents brute-force password attacks. Wait for the timeout or ask the manager to unlock it.

### Change my password
Click the key icon next to your name → enter your current password and the new one twice.

---

## 5. Users: Manager and Cashier

| Action | Manager | Cashier |
| :--- | :---: | :---: |
| Sell, open register, cash-in, and cash-out | ✔ | ✔ |
| View dashboard, history, and products | ✔ | ✔ |
| Cancel sale, register/edit/delete product, view profit, export CSV, close register | ✔ | 🔒 *(Requires manager password)* |
| Settings, backup, users, and security | ✔ | ✘ *(Hidden from menu)* |

### Creating a user for an employee
1. Log in as manager → **Security** menu → **New user**.
2. Fill in name and username, select the **Cashier (operator)** role and an initial password.
3. Leave **"Require password change on first login"** checked. This way the employee creates their own password, and even you won't know it.

### Employee forgot their password
Manager → **Security** → on the user's row, click the key (**Reset password**) → set a temporary password. On next login, they are forced to change it.

### Employee left the store
Manager → **Security** → pencil (**Edit**) → uncheck **Active account**. Their sales history is preserved.

💡 The system always requires at least **one active manager**. Recommended: have two managers (e.g., father and son). If one forgets the password, the other can reset it.

---

## 6. Daily routine: opening the register
1. Log in with your username.
2. Go to **Cash Register** (or press `F9`).
3. Enter the change fund amount, meaning how much cash is in the drawer to start (e.g., `50.00`).
4. Click **Open register**. The top bar will display ● **Register open** along with today's total sales.

*With the register closed, the sales screen remains locked.*

---

## 7. Making a sale
1. Go to **New sale** (`F2`).
2. Add products using one of these methods:
   * Click the product card.
   * Type the code (or scan the barcode) and press **Enter**.
   * Fast quantity: type `5*40` and **Enter** to add 5 units of code 40. Or type just `5*` and **Enter**, and the next clicked product will be added 5 times.
3. In the cart, adjust quantities using `−` and `+` or by typing. Setting quantity to zero removes the item.
4. Optionally, enter an **Extra discount (R$)**.
5. Click **Finalize payment** (`F4`).

### Payment Screen
- **Choose method:** Cash, Pix, Debit, Credit, or Mixed (or `Alt + 1` to `5`).
- **Cash:** enter how much the customer gave (or use buttons `+10`, `+20`, `+50`, `+100`). Change is calculated instantly.
- **Pix:** displays the store's Pix key (configured in Settings).
- **Mixed:** split the amount across payment methods. Change can only be given in cash.
- Customer name and Tax ID (CPF/CNPJ) are optional. If a document is entered, the system validates it.
- Click **Confirm sale** (or **Enter**). The receipt is sent to the printer (80mm thermal format). Inventory is deducted automatically.

---

## 8. Cash in, cash out, and closing the register
- **Cash-in (Suprimento):** adding cash to the drawer (e.g., extra change). Cash Register → Cash-in → amount and reason.
- **Cash-out (Sangria):** withdrawing cash (e.g., paying a supplier, bank deposit). Cash Register → Cash-out. Cannot withdraw more than expected in the drawer.

### Closing the register (End of day)
1. **Cash Register** → **Close register**. If you are logged in as a Cashier, a manager must enter their password.
2. The system displays what should be in the drawer (fund + cash sales + cash-ins − cash-outs) and totals for Pix, Debit, and Credit.
3. Count the cash and type the counted amount. It indicates if it matched, had a surplus, or a shortage.
4. **Confirm closing**. The summary is saved under **Previous registers**.

---

## 9. Products and inventory
1. **Products** menu → **New product**. Cashier role requires manager password authorization.
2. Fill in: barcode (optional, must be unique), name*, category*, unit, cost, selling price*, current stock, and minimum stock.
3. Save.
- When stock drops to or below the minimum, the product turns red and appears in the **Low stock** dashboard list.
- The **Margin** column displays profit per unit (price − cost).

---

## 10. Promotions

| Type | Where to configure | How it works |
| :--- | :--- | :--- |
| **By Quantity** | Settings → Quantity Promotion + check "Eligible for quantity promotion" on the product | When marked items reach the minimum threshold (e.g., 15), all apply the promo price. Pix and Cash only. |
| **By Date** | Product → "Date promotion" | Lower price active between start and end dates. |
| **By Payment Method** | Product → "Special price by payment method" | E.g., special price exclusively when paid in cash. |

---

## 11. History, cancellation, and reports
- **History:** Filter by period, status, sale number, customer, or operator.
- **Reprint receipt:** Printer icon.
- **Cancel sale:** `✕` icon → manager password → reason. Inventory is restored, and the sale is marked out with a strikethrough.
- **Export CSV (Excel compatible):** Requires manager password.
- **Dashboard:** Today's revenue, sales count, monthly average ticket, 7-day chart, and low stock items. The **View profit** button (`Ctrl + L`) shows daily profit (requires manager).

---

## 12. Settings and backup
- **Store info:** Name, Tax ID (CNPJ), phone, address, Pix key, and receipt footer message.
- **Backup (Do this weekly!):** **Settings** → **Make backup**. Downloads a file named `Backup_SmartPOS_YYYY-MM-DD.json`.
- **Restore:** Select the backup file → confirm with your password.
- **Factory Reset:** Erases ALL data on this computer. Requires typing confirmation and password.

---

## 13. Security and audit
- **Users:** Create, edit, deactivate, unlock, and reset passwords.
- **Auto-lock screen after inactivity:** Never, 2, 5, 10, 15, or 30 minutes.
- **New recovery code:** Generates a new code and invalidates the previous one (requires password).
- **Audit:** Lists who did what and when (logins, sales, cancellations, etc.). Filterable and exportable to CSV.

---

## 14. Keyboard shortcuts
| Key | Action |
| :--- | :--- |
| `F2` | New sale (focus search bar) |
| `F4` | Finalize payment |
| `F8` | Clear cart |
| `F9` | Cash register screen |
| `Ctrl + L` | Show/hide profit |
| `Ctrl + Shift + L` | Lock screen |
| `Alt + 1` to `5` | Payment methods: Cash, Pix, Debit, Credit, Mixed |
| `Enter` | Confirm sale |
| `Esc` | Close window / clear fast quantity |

---

## 15. Common issues
- **"I forgot the manager password":** Use the recovery code on the login screen or ask another manager to reset it in **Security**.
- **"Opened and everything is empty":** Ensure you are using the same browser and profile; otherwise, restore your latest weekly backup file.

---

## 16. For developers
- **Structure:** Single-file application containing CSS variables, HTML views, and modular JavaScript using local storage (`localStorage`).
- **Storage:** Data managed locally with integer cents to prevent rounding floats.
- **Security:** PBKDF2-SHA256 password encryption and strict input sanitization.

---

***

# 🍋 SmartPOS - Manual do Sistema (PT-BR)
Guia completo: como abrir, criar o login e a senha, vender, controlar o caixa, cadastrar produtos e manter tudo seguro.

## Índice
1. O que vem no pacote
2. Como abrir o programa
3. Primeiro acesso: criar login e senha
4. Entrar, sair e bloquear a tela
5. Usuários: Gerente e Caixa
6. Rotina do dia: abrir o caixa
7. Fazer uma venda
8. Suprimento, sangria e fechamento do caixa
9. Produtos e estoque
10. Promoções
11. Histórico, cancelamento e relatórios
12. Configurações e backup
13. Segurança e auditoria
14. Atalhos de teclado
15. Problemas comuns
16. Para quem vai programar

---

## 1. O que vem no pacote
| Arquivo | Para que serve |
| :--- | :--- |
| `index.html` | O programa. É só um arquivo, sem instalação e sem internet. |
| `MANUAL.md` | Este manual. |
| `README.md` | Resumo técnico do projeto. |

---

## 2. Como abrir o programa
1. Extraia o arquivo ZIP: clique com o botão direito no arquivo → Extrair tudo…
2. Coloque a pasta em um local fixo, por exemplo `Documentos\POS`. Não mude o arquivo de lugar depois.
3. Dê dois cliques em `index.html`. Ele abrirá no seu navegador web.
4. Use sempre o mesmo navegador (Chrome, Edge ou Brave atualizado).

💡 **Dica:** Arraste o arquivo para a barra de favoritos ou crie um atalho na área de trabalho para abrir rápido todos os dias.

**Onde os dados ficam armazenados?** Produtos, vendas, caixas e usuários ficam salvos dentro do navegador deste computador, e não no arquivo em si. Por isso:
- Abrir em outro navegador ou em outro computador mostrará o sistema vazio.
- "Limpar dados de navegação / cookies" no navegador apaga tudo.
- **Faça backups semanais.**

---

## 3. Primeiro acesso: criar login e senha
O sistema não vem com usuário nem senha padrão. Na primeira vez que abrir, ele exibirá a tela "Bem-vindo!" para você criar a conta do Gerente (o dono do sistema).

1. **Nome da loja:** Aparece no topo e no cupom fiscal.
2. **Seu nome:** Exemplo: "João Resende".
3. **Usuário:** O que você digita para entrar. Use apenas letras minúsculas, números, pontos, hífens ou sublinhados, de 3 a 32 caracteres (ex.: `joao`, `joao.resende`).
4. **Senha:** No mínimo 8 caracteres, contendo letras e números. A barra colorida indica a força da senha.
   * Não pode conter o seu nome de usuário nem ser uma senha óbvia (como `12345678` ou `senha123`).
   * Exemplo de senha forte: misture maiúsculas, minúsculas, números e símbolos (crie a sua!).
5. Repita a senha em **Confirmar senha** e clique em **Criar conta e entrar**.

⚠️ **MUITO IMPORTANTE: Código de recuperação**
Logo após criar a conta, aparecerá um código como este: `ABCD-EFGH-JKLM-NPQR`.
- Anote em um papel e guarde em um local seguro.
- É a única maneira de recuperar o acesso caso o gerente esqueça a senha.
- Ele não será exibido novamente. Se perder, gere um novo em **Segurança** enquanto ainda se lembrar da senha.

---

## 4. Entrar, sair e bloquear a tela

### Entrar
Digite seu usuário e senha e clique em **Entrar**. O ícone de olho (`👁`) ao lado da senha revela o que você digitou. Se aparecer "Caps Lock ativado", desligue a tecla.

### Sair
No canto inferior esquerdo, ao lado do seu nome, clique no ícone de saída (seta para fora). No celular, ele fica localizado no topo.

### Bloquear a tela (pausa rápida)
Clique no ícone de cadeado no topo ou pressione `Ctrl + Shift + L`. Para retornar, basta digitar sua senha e o carrinho estará exatamente onde você deixou.
A tela também bloqueia sozinha após 10 minutos de inatividade (esse tempo pode ser alterado em **Segurança**).

### Errou a senha muitas vezes?
Após 5 tentativas incorretas, a conta é bloqueada por 5 minutos. Se errar novamente, o tempo dobra (10, 20, 40 min..., até 1 hora), prevenindo ataques de força bruta. Aguarde o tempo limite ou peça para o gerente desbloquear.

### Alterar minha senha
Clique no ícone de chave ao lado do seu nome → informe sua senha atual e digite a nova duas vezes.

---

## 5. Usuários: Gerente e Caixa

| Ação | Gerente | Caixa |
| :--- | :---: | :---: |
| Vender, abrir o caixa, suprimento e sangria | ✔ | ✔ |
| Ver painel, histórico e produtos | ✔ | ✔ |
| Cancelar venda, cadastrar/editar/excluir produto, ver lucro, exportar CSV, fechar o caixa | ✔ | 🔒 *(Exige senha do gerente)* |
| Configurações, backup, usuários e segurança | ✔ | ❌ *(Oculto do menu)* |

### Criando um usuário para um funcionário
1. Entre como gerente → menu **Segurança** → **Novo usuário**.
2. Preencha nome e usuário, selecione o perfil **Caixa (operador)** e uma senha inicial.
3. Deixe marcado **"Exigir troca de senha no primeiro acesso"** para que o funcionário crie a própria senha, garantindo que nem você a conheça.

### Funcionário esqueceu a senha
Gerente → **Segurança** → na linha do usuário, clique na chave (**Redefinir senha**) → defina uma senha temporária. No próximo login, ele será obrigado a alterá-la.

### Funcionário deixou a loja
Gerente → **Segurança** → lápis (**Editar**) → desmarque **Conta ativa**. O histórico de vendas dele será preservado.

💡 O sistema sempre exige pelo menos **um gerente ativo**. Recomendado: tenha dois gerentes (ex.: pai e filho). Se um esquecer a senha, o outro poderá redefini-la.

---

## 6. Rotina do dia: abrir o caixa
1. Faça login com o seu usuário.
2. Vá em **Caixa** (ou pressione `F9`).
3. Informe o fundo de troco, ou seja, quanto dinheiro há na gaveta para iniciar o dia (ex.: `50,00`).
4. Clique em **Abrir caixa**. A barra superior exibirá ● **Caixa aberto** junto com o total de vendas do dia.

*Com o caixa fechado, a tela de vendas permanece bloqueada.*

---

## 7. Realizando uma venda
1. Vá em **Nova venda** (`F2`).
2. Adicione produtos usando um destes métodos:
   * Clique no cartão do produto.
   * Digite o código (ou passe o leitor de código de barras) e pressione **Enter**.
   * Quantidade rápida: digite `5*40` e **Enter** para adicionar 5 unidades do código 40. Ou digite apenas `5*` e **Enter**, e o próximo produto clicado será adicionado 5 vezes.
3. No carrinho, ajuste as quantidades usando `−` e `+` ou digitando. Definir a quantidade como zero remove o item.
4. Opcionalmente, informe um **Desconto extra (R$)**.
5. Clique em **Finalizar pagamento** (`F4`).

### Tela de Pagamento
- **Escolha a forma:** Dinheiro, Pix, Débito, Crédito ou Misto (ou `Alt + 1` a `5`).
- **Dinheiro:** informe quanto o cliente deu (ou use os botões rápidos `+10`, `+20`, `+50`, `+100`). O troco é calculado na hora.
- **Pix:** exibe a chave Pix da loja (configurada em Configurações).
- **Misto:** divide o valor entre as formas de pagamento. O troco só pode ser dado em dinheiro.
- Nome do cliente e CPF/CNPJ são opcionais. Se um documento for preenchido, o sistema faz a validação automática.
- Clique em **Confirmar venda** (ou **Enter**). O recibo é enviado para a impressora (formato térmico 80mm) e o estoque é dado baixa automaticamente.

---

## 8. Suprimento, sangria e fechamento do caixa
- **Suprimento:** adicionar dinheiro à gaveta (ex.: reforço de troco). Caixa → Suprimento → valor e motivo.
- **Sangria:** retirar dinheiro (ex.: pagamento de fornecedor, depósito bancário). Caixa → Sangria. Não é permitido retirar mais do que o saldo atual previsto na gaveta.

### Fechamento do caixa (Fim do dia)
1. **Caixa** → **Fechar caixa**. Se estiver logado como Caixa, um gerente precisará inserir a senha.
2. O sistema exibe o valor esperado na gaveta (fundo + vendas em dinheiro + suprimentos − sangrias) e os totais de Pix, Débito e Crédito.
3. Conte o dinheiro físico e digite o valor contado. O sistema indica se bateu exato, se houve sobra ou falta.
4. **Confirmar fechamento**. O resumo fica salvo em **Caixas anteriores**.

---

## 9. Produtos e estoque
1. Menu **Produtos** → **Novo produto** (perfil de Caixa exige autorização com senha de gerente).
2. Preencha: código de barras (opcional, deve ser único), nome*, categoria*, unidade, custo, preço de venda*, estoque atual e estoque mínimo.
3. Salvar.
- Quando o estoque atinge ou fica abaixo do mínimo, o produto fica vermelho e aparece na lista de **Estoque baixo** no painel.
- A coluna **Margem** exibe o lucro por unidade (preço de venda menos custo).

---

## 10. Promoções

| Tipo | Onde configurar | Como funciona |
| :--- | :--- | :--- |
| **Por quantidade** | Configurações → Promoção por quantidade + marcar "Entra na promoção por quantidade" no produto | Quando os itens marcados atingem o limite mínimo (ex.: 15), todos aplicam o preço promocional (somente Pix e Dinheiro). |
| **Por data** | Produto → "Promoção por data" | Preço mais baixo ativo entre a data de início e fim. |
| **Por forma de pagamento** | Produto → "Preço especial por forma de pagamento" | Ex.: preço mais barato exclusivo para pagamentos em dinheiro. |

---

## 11. Histórico, cancelamento e relatórios
- **Histórico:** Filtre por período, status, número da venda, cliente ou operador.
- **Reimprimir recibo:** Ícone de impressora.
- **Cancelar venda:** Ícone `✕` → senha de gerente → motivo. O estoque é estornado e a venda fica marcada como cancelada (não é apagada).
- **Exportar CSV (compatível com Excel):** Requer senha de gerente, por conter lucros e documentos de clientes.
- **Painel:** Faturamento do dia, contagem de vendas, ticket médio mensal, gráfico de 7 dias e itens com estoque baixo. O botão **Ver lucro** (`Ctrl + L`) exibe o lucro diário (exige gerente).

---

## 12. Configurações e backup
Menu **Configurações** (Apenas Gerente):
- **Dados da loja:** Nome, CNPJ, telefone, endereço, chave Pix e mensagem de rodapé do cupom.
- **Backup (Faça semanalmente!):** **Configurações** → **Fazer backup**. Baixa um arquivo chamado `Backup_SmartPOS_AAAA-MM-DD.json`.
- **Restaurar (ou migrar para outro computador):** **Configurações** → **Restaurar** → selecione o arquivo de backup → confirme com sua senha.
- **Zerar sistema (Zona de perigo):** Apaga TODOS os dados deste computador. Exige digitar `APAGAR` e a senha. Faça backup antes.

---

## 13. Segurança e auditoria
Menu **Segurança** (Apenas Gerente):
- **Usuários:** Criar, editar, desativar, desbloquear e redefinir senhas.
- **Bloqueio automático por inatividade:** Nunca, 2, 5, 10, 15 ou 30 minutos.
- **Novo código de recuperação:** Gera um novo código e invalida o anterior (exige senha).
- **Auditoria:** Lista quem fez o quê e quando (logins, senhas incorretas, vendas, cancelamentos, eventos de caixa, produtos, configurações). Filtrável e exportável para CSV.

### Recursos de segurança embutidos
- Proteção de senhas via **PBKDF2-SHA256** (600.000 iterações), padrão da indústria.
- Limitação de tentativas (brute-force throttling), bloqueio automático de tela e troca obrigatória de senhas temporárias.
- Aplicação totalmente offline: sem acesso à internet, dados estritamente locais.

---

## 14. Atalhos de teclado
| Tecla | Ação |
| :--- | :--- |
| `F2` | Nova venda (foca na barra de pesquisa) |
| `F4` | Finalizar pagamento |
| `F8` | Limpar carrinho |
| `F9` | Tela de controle de caixa |
| `Ctrl + L` | Mostrar / ocultar lucro |
| `Ctrl + Shift + L` | Bloquear tela |
| `Alt + 1` a `5` | Formas de pagamento: Dinheiro, Pix, Débito, Crédito, Misto |
| `Enter` (no pagamento) | Confirmar venda |
| `Esc` | Fechar janela / limpar quantidade rápida |

---

## 15. Problemas comuns
- **"Esqueci a senha do gerente":** Na tela de login → **Esqueci minha senha** → informe usuário + código de recuperação + nova senha.
- **"Conta bloqueada":** Aguarde o tempo de espera ou peça a um gerente em **Security** → **Editar** → **Desbloquear tentativas**.
- **"Abri e está tudo vazio":** Você provavelmente abriu em outro navegador, aba anônima ou os dados do navegador foram limpos. Restaure o último backup.
- **"Impressora não funciona":** Usa a caixa de diálogo de impressão padrão do navegador. Ajuste para impressora térmica, papel 80mm e margens "Nenhuma".

---

## 16. Para quem vai programar
- **Estrutura:** Aplicação de arquivo único contendo variáveis CSS, visual HTML e script JavaScript modular integrado ao armazenamento local (`localStorage`).
- **Armazenamento:** Valores monetários armazenados estritamente em centavos inteiros para evitar erros de ponto flutuante.
- **Segurança:** Encriptação de senhas via PBKDF2-SHA256 e higienização de entradas de texto.

---
*SmartPOS, version 2 · Desenvolvido por João Victor Mendes Resende · E-mail: joaoresende270309@gmail.com*
