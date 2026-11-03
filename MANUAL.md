# 🍋 Polpas Sul POS Manual
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
2. Place the folder in a fixed location, e.g., `Documents\POS`. Do not move the file afterwards (see warning below).
3. Double-click `index.html`. It will open in your web browser.
4. Always use the same browser (updated Chrome, Edge, or Brave).

💡 **Tip:** Drag the file to your bookmarks bar, or create a shortcut on your desktop, to open it quickly every day.

**Where is the data stored?** Products, sales, cash registers, and users are stored inside the browser of this computer, not in the file itself. Therefore:
* Opening it in another browser or on another computer will show an empty system.
* Clearing browsing data/cookies in the browser will erase everything.
* **Make backups weekly.**

---

## 3. First access: create login and password
The system does not come with a default user or password. The first time you open it, it displays the "Welcome!" screen for you to create the Manager account (the system owner).

1. **Store name:** Appears at the top and on the receipt.
2. **Your name:** E.g., "João Resende".
3. **Username:** What you type to sign in. Use only lowercase letters, numbers, dots, hyphens, or underscores, 3 to 32 characters long. Examples: `joao`, `maria.silva`.
4. **Password:** At least 8 characters, containing letters and numbers. The colored bar shows password strength.
   * Cannot contain your username or be an obvious password (like `12345678` or `password123`).
   * Strong password example: mix uppercase, lowercase, numbers, and symbols, e.g., `Polpa#Sul2026` (create your own!).
5. Repeat the password in **Confirm password** and click **Create account and sign in**.

⚠️ **VERY IMPORTANT: Recovery Code.** Right after creating the account, a code like this appears: `ABCD-EFGH-JKLM-NPQR`.
* Write it down on paper and store it in a safe place.
* It is the only way to recover access if the manager forgets the password.
* It will not be shown again. If you lose it, generate a new one in **Security** while you still remember your password.

*(If you used the old version with a 4-digit PIN, your products, sales, and registers are still there. Only the PIN has been removed).*

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
* **Choose method:** Cash, Pix, Debit, Credit, or Mixed (or `Alt + 1` to `5`).
* **Cash:** enter how much the customer gave (or use buttons `+10`, `+20`, `+50`, `+100`). Change is calculated instantly.
* **Pix:** displays the store's Pix key (configured in Settings).
* **Mixed:** split the amount across payment methods. Change can only be given in cash.
* Customer name and Tax ID (CPF/CNPJ) are optional. If a document is entered, the system validates it.
* Click **Confirm sale** (or **Enter**). The receipt is sent to the printer (80mm thermal format). Inventory is deducted automatically.

💡 The price shown in the cart already accounts for Cash/Pix discounts. If the customer pays by card, the total may change on the payment screen.

---

## 8. Cash in, cash out, and closing the register
* **Cash-in (Suprimento):** adding cash to the drawer (e.g., extra change). Cash Register → Cash-in → amount and reason.
* **Cash-out (Sangria):** withdrawing cash (e.g., paying a supplier, bank deposit). Cash Register → Cash-out. Cannot withdraw more than expected in the drawer.
* Each movement is listed with time and responsible user.

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
* When stock drops to or below the minimum, the product turns red and appears in the **Low stock** dashboard list.
* The system allows selling without stock (with a warning), resulting in negative inventory.
* **Delete:** A product with sales history cannot be deleted (to preserve records), but it can be deactivated.
* The **Margin** column displays profit per unit (price − cost).

---

## 10. Promotions

| Type | Where to configure | How it works |
| :--- | :--- | :--- |
| **By Quantity** | Settings → Quantity Promotion + check "Eligible for quantity promotion" on the product | When marked items reach the minimum threshold (e.g., 15), all apply the promo price (e.g., R$ 1.00). Pix and Cash only. |
| **By Date** | Product → "Date promotion" | Lower price active between start and end dates. |
| **By Payment Method** | Product → "Special price by payment method" | E.g., cheaper water exclusively when paid in cash. |

The receipt prints **"You saved R$ X"** whenever a promotion is applied.

---

## 11. History, cancellation, and reports
* **History:** Filter by period, status, sale number, customer, or operator.
* **Reprint receipt:** Printer icon.
* **Cancel sale:** `✕` icon → manager password → reason. Inventory is restored, and the sale is marked out with a strikethrough (not deleted).
* **Export CSV (Excel compatible):** Requires manager password, as it contains profits and customer tax IDs.
* **Dashboard:** Today's revenue, sales count, monthly average ticket, 7-day chart, and low stock items. The **View profit** button (`Ctrl + L`) shows daily profit (requires manager).

---

## 12. Settings and backup
**Settings** menu (Manager only):
* **Store info:** Name, Tax ID (CNPJ), phone, address, Pix key, and receipt footer message.
* **Quantity promotion** (see section 10).

### Backup (Do this weekly!)
1. **Settings** → **Make backup**. Downloads a file named `Backup_PolpasSul_YYYY-MM-DD.json`.
2. Copy this file to a USB drive or Google Drive/OneDrive.

The backup includes users and audit logs, but never raw passwords—only a hashed version that cannot be reversed.

### Restore (or move to another computer)
1. On the new computer, open the POS. If the "Welcome" screen appears, create any temporary manager.
2. **Settings** → **Restore** → select the backup file → confirm with your password.
3. After reloading, log in with a user that existed in the backup.

**Factory Reset (Danger zone):** Erases ALL data on this computer. Requires typing `APAGAR` and password. Make a backup first.

---

## 13. Security and audit
**Security** menu (Manager only):
* **Users:** Create, edit, deactivate, unlock, and reset passwords.
* **Auto-lock screen after inactivity:** Never, 2, 5, 10, 15, or 30 minutes.
* **New recovery code:** Generates a new code and invalidates the previous one (requires password).
* **Audit:** Lists who did what and when (logins, incorrect passwords, sales, cancellations, register events, products, settings). Filterable and exportable to CSV.

### Security features built-in
* Passwords protected via **PBKDF2-SHA256** (600,000 iterations), an industry standard.
* Brute-force throttling, auto-lock screen, and forced change of temporary passwords.
* Protection against malicious injection in product/customer names and spreadsheet formula injection.
* Fully offline application: zero internet access, data stays strictly local.

*Honest limitation:* Data is stored inside the browser without disk encryption. Local authentication protects day-to-day operations (employees, counter customers), but anyone with full computer access and technical skills can bypass browser storage. To reinforce:
* Set a Windows password and lock your computer (`Windows + L`) when leaving.
* Do not let employees use the manager's Windows account for other tasks.
* Keep regular backups.

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
| `Enter` (in payment) | Confirm sale |
| `Esc` | Close window / clear fast quantity |

---

## 15. Common issues
* **"I forgot the manager password"**
  * On the login screen → **Forgot password** → username + recovery code + new password. A new code will be generated: save it.
  * If another manager is available, they can reset your password via **Security**.
  * Without code and without another manager, recovery is impossible (by design, to prevent breaches). Solution: restore a backup into a fresh setup and log in using a user from that backup.
* **"Account locked"**
  * Wait for the timeout or ask a manager: **Security** → **Edit** → **Unlock login attempts**.
* **"Opened and everything is empty / asking to create an account"**
  * You likely opened it in a different browser, another computer, in incognito mode, or browser data was cleared. Open your regular browser. If data was lost, restore the latest backup.
* **"Printer not working"**
  * Uses the standard browser print dialog. Choose your thermal printer, 80mm paper size, and "None" margins. If you don't have a printer, cancel the dialog: the sale is already saved.
* **"Data changed in another tab warning"**
  * Use the POS in a single tab. Multiple active tabs can cause data overwrites.
* **"Browser unsupported security warning"**
  * Update your browser or use an updated version of Chrome, Edge, or Brave.

---

## 16. For developers
* **Structure:** Single-file application containing `<style>` (UI variables in `:root`, dark theme via `[data-theme="dark"]`), HTML views, and a modular `<script>` divided into annotated blocks: Core, State, Security, Dialog, Auth, Navigation, Cashier, POS, Checkout, Products, History, Dashboard, Print, Settings, Users, Events, and Initialization.
* **Storage:** `localStorage` prefixed with `polpas_sul_` (`products`, `sales`, `cashHistory`, `currentRegister`, `settings`, `users`, `audit`, `cart`). Currency values stored strictly in integer cents.
* **UI Actions:** Buttons use `data-action="name"`, bound via the `ACTIONS` dictionary (no inline `onclick` attributes).
* **Permissions:** `can('perm')` and `await authorize('perm', 'description')`. Operators are restricted to `vender`, `abrir_caixa`, `suprimento`, and `sangria` (`PERMS` object).
* **Security Rule:** All user-supplied strings entering `innerHTML` must pass through `esc()`.
* **Audit trail:** Log critical actions using `audit('action', 'details')` and register new labels in `AUDIT_LABELS`.
* **Testing:** To test safely without altering production data, use a separate browser profile or an incognito window.
* **Next evolution (scaling):** Introduce a backend database (e.g., Supabase/Firebase) to support multi-terminal operations and encrypted storage.

---
*Polpas Sul POS, version 2 · Developed by João Victor Mendes Resende · User Manual*E-mail: joaoresende270309@gmail.com





PT BR
🍋 Manual do PDV Polpas Sul

Guia completo: como abrir, criar o login e a senha, vender, controlar o caixa, cadastrar produtos e manter tudo seguro.

Índice

O que vem no pacote

Como abrir o programa

Primeiro acesso: criar login e senha

Entrar, sair e bloquear a tela

Usuários: Gerente e Caixa

Rotina do dia: abrir o caixa

Fazer uma venda

Suprimento, sangria e fechar o caixa

Produtos e estoque

Promoções

Histórico, cancelamento e relatórios

Configurações e backup

Segurança e auditoria

Atalhos de teclado

Problemas comuns

Para quem vai programar

1. O que vem no pacote

Arquivo

Para que serve

PDV Polpas Sul.html

O programa. É só um arquivo, sem instalação e sem internet.

MANUAL.md

Este manual.

README.md

Resumo técnico do projeto.

2. Como abrir o programa

Extraia o ZIP: clique com o botão direito no arquivo → Extrair tudo…

Coloque a pasta num lugar fixo, por exemplo Documentos\PDV. Não mude o arquivo de lugar depois.

Dê dois cliques em PDV Polpas Sul.html. Ele abre no navegador.

Use sempre o mesmo navegador (Chrome, Edge ou Brave atualizado).

💡 Dica: Arraste o arquivo para a barra de favoritos, ou crie um atalho na área de trabalho, para abrir rápido todo dia.

Onde ficam os dados?

Produtos, vendas, caixas e usuários ficam guardados dentro do navegador deste computador, não no arquivo. Por isso:

Abrindo noutro navegador ou noutro computador, o sistema aparece vazio.

"Limpar dados de navegação / cookies" no navegador apaga tudo.

Faça backup toda semana.

3. Primeiro acesso: criar login e senha

O sistema não vem com usuário nem senha prontos. Na primeira vez que abrir, ele mostra a tela "Bem-vindo!" para você criar a conta do Gerente, o dono do sistema.

Nome da loja: aparece no topo e no cupom.

Seu nome: por exemplo, João Resende.

Usuário: é o que você digita para entrar. Use só letras minúsculas, números, ponto, hífen ou sublinhado, de 3 a 32 caracteres (ex.: joao, joao.resende).

Senha: no mínimo 8 caracteres, com letras e números. A barrinha colorida mostra a força da senha.

Não pode conter o nome de usuário nem ser uma senha óbvia (como 12345678 ou senha123).

Senha forte: misture maiúsculas, minúsculas, números e símbolos (crie a sua!).

Repita a senha em Confirmar senha e clique em Criar conta e entrar.

⚠️ MUITO IMPORTANTE: Código de recuperação
Logo depois de criar a conta, aparece um código assim: ABCD-EFGH-JKLM-NPQR.

Anote no papel e guarde em local seguro.

É a única forma de recuperar o acesso se o gerente esquecer a senha.

Ele não aparece de novo. Se perder, gere outro em Segurança enquanto ainda lembra a senha.

Se você já usava a versão antiga (com PIN de 4 dígitos), seus produtos, vendas e caixas continuam lá. Só o PIN deixa de existir.

4. Entrar, sair e bloquear a tela

Entrar: Digite usuário e senha e clique em Entrar. O ícone do olho ($👁$) ao lado da senha mostra o que você digitou. Se aparecer "Caps Lock ativado", desligue a tecla.

Sair: No canto inferior esquerdo, ao lado do seu nome, clique no ícone de saída (seta para fora). No telemóvel/celular, fica no topo.

Bloquear a tela (pausa rápida): Clique no cadeado no topo ou aperte Ctrl + Shift + L. Para voltar, basta digitar a senha; o carrinho continua onde estava. A tela também trava sozinha após 10 minutos sem uso (o tempo pode ser mudado em Segurança).

Errou a senha várias vezes? Após 5 tentativas erradas, a conta fica bloqueada por 5 minutos. Se errar de novo, o tempo dobra (10, 20, 40 min... até 1 hora). Espere o tempo ou peça ao gerente para desbloquear.

Trocar a minha senha: Clique no ícone de chave ao lado do seu nome $\rightarrow$ informe a senha atual e a nova duas vezes.

5. Usuários: Gerente e Caixa

Ação

Gerente

Caixa

Vender, abrir o caixa, suprimento e sangria

✔

✔

Ver painel, histórico e produtos

✔

✔

Cancelar venda, cadastrar/editar/excluir produto, ver lucro, exportar CSV, fechar o caixa

✔

🔒 (Pede senha do gerente)

Configurações, backup, usuários e segurança

✔

❌ (Não aparece no menu)

Criar um utilizador/funcionário

Entre como gerente $\rightarrow$ menu Segurança $\rightarrow$ Novo usuário.

Preencha nome e usuário, escolha o perfil Caixa (operador) e uma senha inicial.

Deixe marcado "Pedir para trocar a senha no primeiro acesso" para que ele crie a própria senha.

Esqueceu a senha: Gerente $\rightarrow$ Segurança $\rightarrow$ clique na chave (Redefinir senha) $\rightarrow$ defina uma senha temporária.

Funcionário saiu da loja: Gerente $\rightarrow$ Segurança $\rightarrow$ lápis (Editar) $\rightarrow$ desmarque Conta ativa. O histórico de vendas dele é mantido.

💡 Dica: O sistema exige pelo menos um gerente ativo. Recomendado: tenha dois gerentes. Se um esquecer a senha, o outro redefine.

6. Rotina do dia: abrir o caixa

Entre com o seu usuário.

Vá em Caixa (ou aperte F9).

Digite o fundo de troco (quanto dinheiro tem na gaveta ao começar, ex.: 50,00).

Clique em Abrir caixa. No topo aparece ● Caixa aberto e o total vendido no dia.

Nota: Com o caixa fechado, a tela de vendas fica bloqueada.

7. Fazer uma venda

Vá em Nova venda (atalho F2).

Adicione produtos de uma destas formas:

Clique no cartão do produto.

Digite o código (ou passe o leitor de código de barras) e aperte Enter.

Quantidade rápida: digite 5*40 e Enter para colocar 5 unidades do código 40. Ou digite só 5* e Enter, e o próximo produto clicado entra 5 vezes.

No carrinho, ajuste a quantidade com − e + ou digitando. Zerar a quantidade remove o item.

Se quiser, informe um Desconto extra (R$).

Clique em Finalizar pagamento (atalho F4).

Tela de pagamento

Formas: Dinheiro, Pix, Débito, Crédito ou Misto (atalhos Alt + 1 a 5).

Dinheiro: digite quanto o cliente deu (ou use os botões +10, +20, +50, +100). O troco aparece na hora.

Pix: mostra a chave Pix da loja configurada nas definições.

Misto: divide o valor entre as formas. O troco só pode sair do dinheiro.

Cliente e CPF/CNPJ: opcionais. Se digitar o documento, o sistema valida automaticamente.

Clique em Confirmar venda (Enter). O recibo térmico (80 mm) é gerado e o stock baixa de forma automática.

8. Suprimento, sangria e fechar o caixa

Suprimento: colocar dinheiro na gaveta (ex.: mais troco). Vá em Caixa $\rightarrow$ Suprimento $\rightarrow$ informe valor e motivo.

Sangria: retirar dinheiro (ex.: pagar fornecedor, levar ao banco). Vá em Caixa $\rightarrow$ Sangria. Não é permitido retirar mais do que o saldo atual da gaveta.

Fechar o caixa (fim do dia)

Vá em Caixa $\rightarrow$ Fechar caixa. Se for operador de caixa, um gerente precisará inserir a senha.

O sistema mostra o esperado na gaveta e os totais de Pix, Débito e Crédito.

Conte o dinheiro físico e digite o valor contado. O sistema indica se bateu, se sobrou ou se faltou.

Clique em Confirmar fechamento. O resumo fica gravado em "Caixas anteriores".

9. Produtos e estoque

Menu Produtos $\rightarrow$ Novo produto (pede senha de gerente se for operador).

Preencha: código de barras, nome*, categoria*, unidade, custo, preço de venda*, estoque atual e estoque mínimo.

Clique em Salvar.

Estoque baixo: quando atinge o limite mínimo, o produto fica destacado a vermelho no painel.

Margem: o sistema calcula automaticamente o lucro bruto por unidade (venda menos custo).

10. Promoções

Por quantidade: Configurações $\rightarrow$ Ativar promoção por quantidade + marcar "Entra na promoção por quantidade" no produto. Quando atinge o mínimo (ex.: 15 itens), o preço unitário ajusta-se automaticamente (válido para Pix e Dinheiro).

Por data: No produto $\rightarrow$ Definir preço promocional com data de início e fim.

Por forma de pagamento: No produto $\rightarrow$ Definir preço especial exclusivo para determinadas formas de pagamento.

11. Histórico, cancelamento e relatórios

Histórico: filtre por período, status, número da venda, cliente ou operador.

Reimprimir recibo: clique no ícone da impressora.

Cancelar venda: ícone $\times$ $\rightarrow$ exige senha de gerente $\rightarrow$ informe o motivo. O stock retorna automaticamente e a venda fica registada como cancelada.

Exportar CSV: descarrega um relatório completo para abrir no Excel.

Painel: faturamento do dia, total de vendas, ticket médio, gráfico dos últimos 7 dias e botão Ver lucro (Ctrl + L).

12. Configurações e backup

Dados da loja: nome, CNPJ, telefone, morada, chave Pix e mensagem de rodapé do cupom.

Backup semanal (Recomendado): Vá em Configurações $\rightarrow$ Fazer backup. Descarrega um ficheiro .json com todos os dados da loja. Guarde-o num local seguro (Google Drive, OneDrive ou pen drive).

Restaurar: Permite carregar um backup anterior num computador novo.

Zerar sistema: Apaga todos os dados locais do navegador (requer confirmação por palavra-passe e palavra de segurança).

13. Segurança e auditoria

Contas e Permissões: Gestão completa de utilizadores (Gerente e Caixa).

Bloqueio automático: Configurável de 2 a 30 minutos de inatividade.

Código de recuperação: Chave única de 16 caracteres para recuperação de conta de gerente.

Auditoria: Registo detalhado de todas as acções executadas no sistema (logins, vendas, cancelamentos, alterações de stock), com opção de exportação em CSV.

14. Atalhos de teclado

Tecla

Ação

F2

Nova venda (foca na barra de pesquisa)

F4

Finalizar pagamento

F8

Limpar carrinho

F9

Tela de controlo de caixa

Ctrl + L

Mostrar / ocultar o lucro no painel

Ctrl + Shift + L

Bloquear a tela imediatamente

Alt + 1 a 5

Selecionar forma de pagamento (Dinheiro, Pix, Débito, Crédito, Misto)

Enter

Confirmar venda / ações

Esc

Fechar modais / cancelar quantidade rápida

15. Problemas comuns

"Esqueci a senha do gerente": Utilize a opção "Esqueci minha senha" na tela de login informando o código de recuperação de 16 dígitos, ou peça a outro gerente para redefinir na aba de Segurança.

"Abri e está tudo vazio": Verifique se está a usar o mesmo navegador de sempre e se os dados do browser não foram limpos. Se necessário, importe o seu último ficheiro de backup.

16. Para quem vai programar

Arquivo único HTML contendo todo o ecossistema (frontend, estilos CSS e lógica JS em armazenamento local localStorage).

Padrão monetário interno gerido em centavos (inteiros) para evitar erros de arredondamento de vírgula flutuante.

Funções robustas de encriptação com PBKDF2-SHA256 para as palavras-passe.

PDV Polpas Sul · Desenvolvido por João Victor Mendes Resende · E-mail: joaoresende270309@gmail.com
