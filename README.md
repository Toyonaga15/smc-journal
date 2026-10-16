# SMC Trading Journal v1.0

PWA estático, em português, sem servidor ou bibliotecas externas. Funciona offline após primeira abertura online. Todos os dados são guardados no `localStorage` do navegador, no dispositivo e origem (domínio) usados. Não há login nem sincronização.

## Publicar (GitHub Pages)
1. Crie um repositório público no GitHub, por exemplo `smc-journal`.
2. Envie **o conteúdo desta pasta** para a raiz do repositório (`index.html`, `app.js`, `styles.css`, `sw.js`, `manifest.webmanifest`, `icon-192.png`, `icon-512.png`).
3. Abra Settings > Pages > Build and deployment > Deploy from a branch, escolha `main` e `/ (root)`, salve.
4. Aguarde a URL HTTPS do GitHub Pages, por exemplo `https://SEU-USUARIO.github.io/smc-journal/`. A URL real depende do repositório.
5. Abra a URL no Safari do iPhone, toque em Compartilhar > Adicionar à Tela de Início > Adicionar. Se houver a opção "Abrir como app", mantenha ativada.

Alternativa: publicar os mesmos arquivos em qualquer hospedagem estática HTTPS (Netlify, Cloudflare Pages etc.). **Abrir `index.html` diretamente como arquivo não instala o PWA**; é preciso hospedagem HTTPS (ou localhost para desenvolvimento).

## Usar
- Checklist: preencha antes da operação, selecione Planejada ou Aberta e salve.
- Diário: toque em Editar / resultado, marque Fechada e registre R líquido (ex.: +2, -1, +0.4).
- Dashboard: curva de R, win rate, expectativa, profit factor, drawdown e comparação agressiva/confirmada.
- Dados: exporte CSV (delimitado por `;`), Excel (.xlsx) e backup JSON. A importação JSON substitui o histórico atual.

## Limitações importantes
- Dados no navegador podem ser apagados pela limpeza de dados do site, remoção do app ou troca de dispositivo. **Faça backups JSON frequentes**, preferencialmente no app Arquivos/iCloud Drive.
- Estatísticas agregam todas as operações fechadas (real, demo, backtest); separe os ambientes antes de inferir vantagens. A tela Diário permite filtrar ambiente, mas o Dashboard v1 ainda não.
- Resultado em R é informado manualmente, líquido de custos. Campos monetários são opcionais e não são convertidos automaticamente em R.
- Não existe conexão com MT5, TradingView, corretora, push, autenticação ou análise por IA externa.
- Insights são regras locais descritivas, não previsões nem testes de significância estatística.
- Pontuação de checklist é heurística, não chance de acerto. Não substitui gestão de risco.
