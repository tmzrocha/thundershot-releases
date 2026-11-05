# ThunderShot

Captura de tela rápida e local para Windows: selecione, anote e copie em segundos. Funciona com vários monitores e
escalas diferentes, e nenhuma captura sai do seu computador.

Este repositório guarda só os instaladores e as atualizações do app. O código-fonte não é publicado aqui.

**[Baixar a versão mais recente](https://github.com/tmzrocha/thundershot-releases/releases/latest)**

## O que ele faz
- **Capturar:** Print Screen ou Ctrl+Shift+Q. Arraste para selecionar, inclusive entre monitores; Ctrl+A pega a tela
  inteira, e Ctrl+A de novo, todas as telas. Shift+Print Screen repete a última região. Pelo ícone da bandeja, captura
  com atraso de 3, 5 ou 10 segundos.
- **Anotar no próprio overlay:** seta, retângulo, elipse, linha, caneta, marcador, texto, numeração, pixelizar,
  desfocar, destacar área e régua, com painel de cor, espessura e fonte. Ctrl+Z desfaz.
- **Copiar texto da tela (O):** reconhece o texto da seleção no próprio computador e copia como texto.
- **Ocultar dados sensíveis (D):** pixeliza e-mails, telefones, CPF, CNPJ, cartões, chaves de API, tokens, senhas e
  connection strings antes de compartilhar.
- **Moldura (Q):** fundo em degradê, cantos arredondados e sombra, pronta para documentação e apresentações.
- **Saídas:** copiar (Ctrl+C ou Enter), salvar em PNG ou JPG (Ctrl+S), fixar na tela, arrastar para outro app e
  imprimir.
- **Histórico local, opcional:** guarda as capturas no computador, com busca pelo texto delas. Vem desligado.
- **Página inteira no navegador:** páginas longas, como capítulos de webtoon, são capturadas pela extensão do
  ThunderShot para Chrome e Edge, que vem com o app (veja abaixo).

## Instalar
1. Baixe `ThunderShot-<versão>-win-x64-setup.exe` na [versão mais recente](https://github.com/tmzrocha/thundershot-releases/releases/latest).
2. Abra o arquivo. A instalação é só para o seu usuário, não pede administrador e fica em
   `%LOCALAPPDATA%\Programs\ThunderShot`, com atalho no menu Iniciar.
3. O ThunderShot fica na bandeja do Windows, ao lado do relógio. O botão direito no ícone abre o menu, com as
   configurações.

Os instaladores ainda não têm assinatura digital. Na primeira vez, o Windows pode mostrar "O Windows protegeu o
computador": clique em **Mais informações** e depois em **Executar assim mesmo**.

Prefere não instalar? Baixe `ThunderShot-<versão>-win-x64-portable.zip`, extraia numa pasta e abra o
`ThunderShot.exe`.

### Conferir o arquivo baixado (opcional)
Cada versão traz um `SHA256SUMS.txt`. No PowerShell, na pasta do download:

```powershell
Get-FileHash .\ThunderShot-<versão>-win-x64-setup.exe -Algorithm SHA256
```

O resultado tem de ser igual ao que está no `SHA256SUMS.txt` para esse arquivo.

## Página inteira no navegador
A extensão rola a página até o fim, carrega o que só aparece ao rolar e abre a captura numa guia nova, com o botão
**Baixar PNG**: uma imagem só, exatamente como aparece na página. Funciona no Chrome, no Edge e em outros navegadores
baseados no Chromium (Brave, Opera, Vivaldi).

Enquanto ela não está na Chrome Web Store, é carregada pela pasta que vem com o app:
1. No menu do ícone do ThunderShot, escolha **Página inteira no navegador...**. A janela mostra o passo a passo.
2. No navegador, abra `chrome://extensions` (no Edge, `edge://extensions`) e ligue o **Modo do desenvolvedor**.
3. Clique em **Carregar sem compactação** e escolha a pasta `extensao-navegador` dentro da pasta do ThunderShot.
4. Fixe o ícone do ThunderShot na barra do navegador. Na página, clique nele ou aperte **Alt+Shift+T**; clicar de
   novo durante a captura para antes do fim.

## Atualizações
O ThunderShot procura versão nova ao abrir e uma vez por dia. Quando encontra uma, pergunta antes de instalar. Cada
atualização vem assinada, e o app confere a assinatura antes de instalar; depois ele fecha e abre de novo sozinho. Dá
para desligar a busca automática em **Configurações > Geral** e procurar quando quiser pelo menu do ícone, em
**Procurar atualizações**.

## Privacidade
- **As capturas ficam no seu computador.** Nada é enviado para a internet: o reconhecimento de texto e a ocultação de
  dados sensíveis rodam no próprio Windows.
- **Sem conta e sem telemetria.**
- **Uma única conexão: a busca de versão nova.** Ela consulta só a versão publicada aqui, no GitHub, e pode ser
  desligada.
- **A extensão do navegador também é local.** Ela só age na aba em que você clica no ícone, e a captura fica no próprio
  navegador.

## Iniciar com o Windows
Instalado pelo instalador, o ThunderShot passa a abrir junto com o Windows, a menos que você desmarque a opção na
instalação. Para mudar depois, use o item **Iniciar com o Windows** no menu do ícone ou **Configurações > Geral**.

## Desinstalar
Use **Configurações do Windows > Aplicativos > Aplicativos instalados > ThunderShot > Desinstalar**. A desinstalação
oferece apagar também as preferências e o histórico; as capturas que você salvou ficam onde estão.

## Requisitos
Windows 11, ou Windows 10 versão 2004 ou mais nova, 64 bits.

## Licença
Os termos de distribuição ainda estão em definição. Os componentes de terceiros incluídos e as licenças deles estão
no `THIRD-PARTY-NOTICES.txt`, que acompanha o app, e no `sbom.cdx.json` de cada versão.
