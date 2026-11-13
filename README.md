# Minha Vida Financeira

App de finanças pessoais que funciona direto no navegador e pode ser instalado no celular como um aplicativo (PWA). Não precisa de servidor nem de cadastro: tudo roda no próprio aparelho.

## O que o app faz

- **Reservas/Investimentos:** investimentos por tipo (poupança, ações, títulos, fundos, cripto…), com operações de investir e resgatar. Em ações, informa preço, quantidade e preço médio, e o ganho ou a perda da venda é lançado automaticamente.
- **Contas bancárias e Dinheiro (em espécie):** saldos, transferências entre contas e saques.
- **Entradas e Saídas:** lançamentos por categoria, com categorias recorrentes (ex.: salário).
- **Dívidas e Cartões:** parcelas, assinaturas, faturas de cartão, pagamentos e débito automático.
- **Relatórios:** resumo, entradas, saídas, dívidas/cartões, contas, investimentos, ações e patrimônio, com gráficos e exportação em HTML.
- **Seletor de mês:** Reservas/Investimentos, Contas, Entradas, Saídas, Dívidas e Relatórios permitem consultar meses anteriores. Corrigir um registro antigo ajusta automaticamente os saldos e relatórios dos meses seguintes.
- **Extras:** temas (Padrão, Escuro e Claro), bloqueio por senha/biometria do celular, backup em arquivo `.json` e funcionamento offline.

## Como os dados são guardados

Os dados ficam no `localStorage` do navegador, no próprio aparelho. Nada é enviado para a internet.

Por isso:
- Limpar os dados do navegador apaga o app. Faça backup de vez em quando em **Configurações → Exportar dados**.
- Para trocar de celular, exporte o backup e use **Importar backup** no novo aparelho.
- Computador e celular têm dados separados, a menos que você importe o backup de um no outro.

## Arquivos do projeto

| Arquivo | Função |
|---|---|
| `index.html` | O app inteiro (interface e lógica) |
| `sw.js` | Service worker: faz o app abrir offline |
| `manifest.webmanifest` | Nome, cores e ícones para instalar o app |
| `icon.svg`, `icon-192.png`, `icon-512.png`, `apple-touch-icon.png` | Ícones do app |

## Como testar

### 1. Acessando o site

Abra o endereço publicado do app no navegador celular:

```
https://appminhavidafinanceira.vercel.app
```

Roteiro rápido de teste:

1. Na tela inicial, informe seu nome.
2. Em **Contas bancárias**, cadastre uma conta com saldo.
3. Em **Movimentação financeira → Entradas e Saídas**, registre alguns lançamentos.
4. Use as setas ‹ › no topo das telas para navegar entre meses.
5. Abra **📊 Relatórios** e confira os totais e gráficos.

### 2. Instalando no celular (Chrome, Android)

1. Abra o endereço do app no **Chrome**.
2. Toque no menu **⋮** (canto superior direito).
3. Toque em **Instalar app** (ou **Adicionar à tela inicial**).
4. Confirme. O ícone aparece na tela inicial e o app abre em tela cheia, sem a barra do navegador.

No iPhone (Safari): botão de compartilhar → **Adicionar à Tela de Início**.

> O site precisa ser aberto por **https** para a instalação e o bloqueio por biometria funcionarem.

