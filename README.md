# TranslateGamers

Aplicativo simples para traduzir textos e capturas de tela de jogos usando Google Translate e OCR (Tesseract), com interface em Tkinter.

## Recursos

- Tradução de textos digitados com suporte a origem automática.
- Monitorar clipboard e traduzir automaticamente quando o texto muda.
- OCR de área da tela com seleção visual da região.
- Pré-visualização e histórico de traduções.
- Instalação automática de dependências na primeira execução.
- Pergunta o idioma da interface e de destino na primeira inicialização e mantém nas próximas.
- Interface multilíngue: escolha entre todos os idiomas suportados pelo app.
 - Configurações e diálogos também são traduzidos.
  - Ao trocar o idioma, a interface, listas e Configurações atualizam imediatamente.
- Ao minimizar, aparece um botão flutuante na lateral; clique para restaurar.
- A pré-visualização e o histórico mostram a língua detectada quando a origem é automática.
- Temas: Claro, Escuro, Ocean, Forest; tema Personalizado com seletor de cores.
- Fontes configuráveis: escolha fontes do Windows (inclui Jokerman) e tamanho.

## Requisitos

- Windows com Python 3.11 ou superior instalado e acessível em `PATH`.
- Para OCR: Tesseract-OCR instalado no Windows.
  - Baixe em: https://github.com/UB-Mannheim/tesseract/wiki
  - O aplicativo tenta detectar automaticamente em `C:\\Program Files\\Tesseract-OCR\\tesseract.exe`.

## Como usar

1. Baixe/clique duas vezes para abrir `TranslateGamers.exe.py` com Python.
2. Na primeira execução, selecione o idioma de destino.
3. Digite texto e clique em `Traduzir` ou habilite `Traduzir enquanto digita`.
4. Em `⚙ Configurações`:
   - `Monitorar clipboard`: traduz o conteúdo copiado.
   - `Selecionar área (x,y,w,h)`: define manualmente a região do OCR.
   - `Selecionar área visual`: selecione com o mouse a área da tela.
   - `Iniciar/Parar OCR`: inicia o reconhecimento e tradução contínua.
   - `Idioma da interface`: altere a língua da UI; aplica imediatamente e guarda.
   - `Lado do botão flutuante`: escolha esquerda ou direita para o botão de restauração.
   - `Tema`: escolha entre Claro, Escuro, Ocean, Forest ou `Personalizado`.
   - `Personalizado`: selecione `Cor de fundo`, `Cor do texto` e `Cor de destaque`.
   - `Fonte` e `Tamanho da fonte`: altere a família e o tamanho aplicados à UI.
   - As mensagens de erro/aviso são exibidas no idioma da interface.

## Observações

- Dependências Python são instaladas automaticamente: `googletrans==4.0.0rc1`, `pyperclip`, `pillow`, `mss`, `pytesseract`, `pystray`.
- Se o Tesseract não estiver no `PATH`, o app tenta localizar em diretórios comuns.
- Configurações são salvas em `~/.translategamers.json`.
- Idiomas disponíveis na interface: Português (`pt`), Inglês (`en`), Espanhol (`es`), Francês (`fr`), Alemão (`de`), Italiano (`it`), Russo (`ru`), Japonês (`ja`), Coreano (`ko`), Chinês Simplificado (`zh-cn`), Chinês Tradicional (`zh-tw`).
- Para idiomas sem pacote de tradução específico, a UI é traduzida automaticamente usando o serviço de tradução com fallback robusto.
 - A tradução de textos usa serviço principal e fallback alternativo para garantir funcionamento.
- Origem automática suportada; se a detecção falhar, um fallback mantém a tradução.
- O tamanho padrão da janela foi ampliado para evitar elementos cobrindo botões.

## Execução por linha de comando

```
python TranslateGamers.exe.py --mode cli --text "hello" --target pt
```

## Créditos

- Criador: Felipenor
- Acesse: https://linkr.bio/Felipenor
- YouTube: https://youtube.com/@Felipenor
- Twitch: https://twitch.tv/Felipenor

## Licença

Sem licença específica definida. Use por sua conta e risco.