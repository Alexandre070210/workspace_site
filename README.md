
# Projeto: Galeria de Personagens (16:9)

Uma pequena página estática que mostra uma trilogia de imagens em formato paisagem 16:9 com uma história em três capítulos. O projeto contém exemplos de prompts para geração de imagens (em `images/prompts_personagens.txt`) e uma galeria responsiva construída com Bootstrap.

Site ao vivo: https://alexandre070210.github.io/workspace_site/

Observação: se você hospedou o site em uma URL diferente (ex.: domínio customizado), substitua o link acima pelo URL correto.

Este repositório foi estruturado com a ajuda de ferramentas de IA (GitHub Copilot e Gemini) para acelerar ideias de conteúdo e organização.

## Objetivo

- Exibir uma galeria responsiva com 3 imagens (panorama 16:9).
- Fornecer prompts prontos em português para gerar imagens semelhantes/evocativas de personagens estilo battle-royale.
- Criar uma apresentação no `index.html` com cartões que apontam separadamente para cada capítulo na `personagens.html`.

## Estrutura do projeto

```
workspace_site/
├─ index.html            # Página principal com apresentação dos cartões
├─ personagens.html      # Galeria + história dividida em 3 capítulos
├─ README.md             # Este arquivo
├─ favoritos_ale.html    # (arquivo existente)
├─ meu_nome.txt          # (arquivo existente)
└─ images/
   ├─ personagens_01.png
   ├─ personagens_02.png
   ├─ personagens_03.png
   └─ prompts_personagens.txt   # Prompts 16:9 e instruções para geradores
```

## Como visualizar (local)

1. Abra `index.html` no navegador (duplo clique) — funciona sem servidor, mas alguns recursos (CSP, fetch) podem exigir um servidor local.
2. Para servir localmente (PowerShell / Windows), use o Python (recomendado se instalado):

```powershell
# a partir da pasta c:\dev_a\workspace_site
python -m http.server 8000
# então abra http://localhost:8000 no navegador
```

Ou use qualquer servidor estático de sua preferência (Live Server do VS Code, http-server do Node, etc.).

## Uso dos prompts

- Os prompts prontos estão em `images/prompts_personagens.txt` — contém 6 sugestões (3 diretas e 3 evocativas), recomendações de parâmetros (Stable Diffusion / Midjourney / Leonardo), e negative prompts.
- Se for gerar imagens com uma ferramenta específica, copie o prompt desejado e ajuste flags/resolução conforme o gerador:
  - Midjourney: adicione `--ar 16:9 --v 5 --q 2` (ou conforme versão).
  - Stable Diffusion (Automatic1111): use 1920x1080, steps 20-40, sampler DPM++/Euler a, cfg 6.5-9.

Observação sobre copyright: prefira as versões "evocativas"/originais se o uso for comercial. Verifique os termos do serviço que você usar.

## Desenvolvimento / próximos passos sugeridos

- Adicionar download funcional (ZIP) com as imagens e link em `personagens.html`.
- Implementar scroll suave para âncoras entre páginas (CSS/JS).
- Transformar a galeria em um carousel para dispositivos móveis.
- Adicionar metadados (og:image, meta description) para melhor compartilhamento.
- Automatizar geração de thumbnails a partir das imagens originais (script Node/Python).

## Contribuindo

1. Faça um fork e crie uma branch com a sua alteração.
2. Envie um pull request descrevendo as mudanças.

Se quiser ajuda para integrar uma feature (ex: carousel, zip automático, ou integração com um serviço de geração de imagens), descreva o que quer e eu ajudo a implementar.

## Créditos

- Estrutura, textos de exemplo e prompts gerados/combinados com suporte de IA: GitHub Copilot e Gemini.
- Código HTML/CSS/Bootstrap: autor do repositório.

## Licença

Sugerimos usar MIT para este tipo de projeto simples. Se concordar, posso adicionar `LICENSE` com o texto MIT.

---

Se quiser, eu já adiciono o arquivo `LICENSE` (MIT), crio o ZIP com as imagens e ativo o link de download em `personagens.html`. Qual desses próximos passos prefere que eu faça agora?
