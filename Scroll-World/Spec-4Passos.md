Resumo dos 4 Passos e Regras de Ouro Extraídos do Vídeo (Já Documentados no Arquivo 17):
Passo 1 — A Imagem Âncora (Ponto de Decisão Crítico):

Tudo nasce de uma única imagem inicial. Todas as cenas seguintes herdam obrigatoriamente a mesma luz, estilo e paleta dessa primeira imagem para que a jornada pareça um filme único e não uma colagem desconexa.

Atenção: O Claude Code vai pausar após gerar essa imagem pedindo sua aprovação. Se algo na estética não agradar, peça para refazer antes de aprovar os vídeos para não gastar créditos à toa.

Passo 2 — Transformação em Vídeo e Movimentos Assinatura (Dive-in / Pull-back):

O Claude Code aciona a Higgsfield via MCP/CLI (usando modelos como GPT Image 2 e Seedance) para transformar a imagem em vídeo com a câmera mergulhando na cena, gerando conectores onde o último quadro de uma cena encaixa perfeitamente no primeiro da seguinte.

Passo 3 — Fatiamento Determinístico com FFmpeg:

O FFmpeg (ferramenta gratuita instalada no seu terminal) fatia os vídeos gerados em dezenas de quadros estáticos (frames), eliminando engasgos de reprodução de vídeo tradicional no navegador.

Passo 4 — Amarração dos Quadros à Barra de Rolagem (scrub-engine.js):

Cada quadro é mapeado a uma posição exata do scroll. Você rola devagar, o filme anda devagar; você para para explicar algo aos jurados, a imagem congela nítida; você volta o scroll, a cena rebobina suavemente.

O que mais o Arquivo 17 traz pronto para você usar:
As 2 Decisões de Orçamento Documentadas: Configurar exatamente 4 cenas (em vez de 6, reduzindo o gasto de créditos sem perder o arco narrativo completo) e ativar o corte seguro crop-safe para mobile (evitando gerar vídeos verticais duplicados).

Prompt Mestre Adaptado (Estilo Diorama de Papel / Origami + Porto Bank): Inspirado no estilo folded paper diorama mostrado no vídeo — que casa perfeitamente com a estética tátil Vox da nossa apresentação — já com as travas para não gerar textos borrados dentro do vídeo e aplicar nossos badges nítidos (/odin:legado, /odin:spec, /odin:build, /odin:cobertura) por cima em HTML/SVG.