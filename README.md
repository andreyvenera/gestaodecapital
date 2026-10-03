# Gestão de Capital

Personal Capital Management. Sistema para organizar contas em real e dólar, imóveis, parcelas, valores a receber e metas de patrimônio, com cotação do dólar e CDI atualizados.

## Como usar

**No GitHub Pages:** o site abre direto. Sem servidor configurado, os dados ficam salvos apenas no navegador de quem usa.

**Com uma planilha Google como banco de dados:**

1. Crie uma planilha nova no Google Drive.
2. Abra Extensões, Apps Script, e cole o conteúdo de `Code.gs`.
3. Execute a função `autorizar` uma vez e aceite as permissões.
4. Implante como App da Web, executando como você, com acesso para qualquer pessoa.
5. Copie a URL que termina em `/exec` e cole em `API_URL`, no início do script do `index.html`.

© 2026 Andrey Marques. All rights reserved.
For personal financial management and record-keeping purposes only.
