# ELO — Portal de direitos das pessoas autistas

Protótipo acadêmico do tema **4.3 — Inclusão Digital e Acessibilidade**, inspirado no trabalho da Comissão de Direito da Pessoa com Autismo da OAB/DF — Subseção Águas Claras. **Não é um site oficial da OAB e não presta consultoria jurídica.**

Adaptação do projeto existente: mantém React, TypeScript, Vite, Tailwind CSS, GSAP/ScrollTrigger, Lucide, o hero editorial, a arte abstrata, o parallax opcional, o menu móvel e os controles de acessibilidade. Não adiciona dependências, backend, autenticação ou coleta de dados pessoais.

## Executar

Node.js 22.12+ e npm (validado com Node 24).

```sh
npm ci
npm run dev
```

No PowerShell com npm.ps1 bloqueado, use `npm.cmd ci` e `npm.cmd run dev` sem alterar as políticas do Windows. O terminal informa a porta usada pelo Vite. Para produção: `npm run build` e `npm run preview`.

## Navegação

1. **Início:** acesso direto a categorias e orientação.
2. **Categorias:** educação; saúde e terapias; planos de saúde; trabalho; benefícios e previdência; isenções; prioridade e acessibilidade. As abas aceitam setas, Home e End e selecionam referências da biblioteca.
3. **Biblioteca:** busca local sem distinção de acentos/maiúsculas, filtro combinado por categoria, contagem, estado vazio e limpeza. Cada referência abre uma explicação, público potencial, caminhos de orientação e fonte oficial.
4. **Situações reais:** cinco painéis expansíveis sobre matrícula, apoio educacional, negativa de plano, BPC e trabalho, com base legal e fontes.
5. **Guia:** cinco assuntos, com três etapas, retorno e reinício, sem solicitar dados, documentos ou diagnósticos. Inclui links de legislação e canais institucionais.
6. **Acessibilidade:** fonte de 100% a 140%, contraste, temas claro/escuro, leitura simplificada, movimento e poucos estímulos. Restaurar configurações retorna ao tema claro e à preferência de movimento do sistema.
7. **Comissão:** atuação descrita no briefing; conteúdo educativo sobre autismo; caráter acadêmico e não oficial explícito.
8. **Encerramento:** mensagem de direitos e espaço para os integrantes.

A nova paleta usa azul #174A83, fundo #F5F8FC e texto #172B45; amarelo #E6B64D, coral #D86A70 e verde-petróleo #377F79 ficam na arte e nos detalhes. Segue a paleta fornecida no briefing; o e-book não foi disponibilizado para análise visual. Não usa peças de quebra-cabeça, fotos remotas ou logotipo oficial da OAB.

## Conteúdo jurídico: revisão pendente

**Nenhuma referência foi apresentada como verificada e vigente.** A consulta ao domínio oficial do Planalto foi bloqueada pela política de rede (CONNECT 403). Os dez registros e as explicações estão marcados como **pendentes de revisão jurídica**, com links para consulta oficial. A inclusão de um link não comprova a vigência ou a aplicabilidade da norma. Também é necessário revisar links e caminhos de orientação antes de uso real.

A seleção local inclui as Leis 12.764/2012, 13.146/2015 e 13.977/2020, além de referências educacionais, de saúde, previdência, assistência social, tributação e prioridade. Não informa artigos, prazos, valores, critérios de renda ou concessão automática de benefícios. A análise de cada caso depende da legislação atual e de orientação profissional.

Dados e fontes ficam em `src/rights.ts`. Biblioteca e explicações ficam em `src/components/RightsLibrary.tsx`. A composição da página e os controles reaproveitados ficam em `src/main.tsx`, e a identidade visual em `src/style.css`.

## Acessibilidade e privacidade

Use Tab/Shift+Tab e Enter/Espaço. Escape fecha o painel; o foco retorna ao botão de abertura. A interação com o fundo é impedida enquanto o painel está aberto. Os limites de fonte preservam o foco do controle. As etapas do guia transferem o foco para o título após uma ação.

O tema inicial é claro. A preferência inicial `prefers-reduced-motion` é respeitada; o controle manual desliga animações GSAP. Poucos estímulos remove apenas decoração e desliga movimentos, preservando textos, fontes jurídicas e controles. A leitura simplificada adapta os resumos sem remover condições, alertas ou links. Preferências, busca e escolhas ficam apenas em memória e reiniciam ao recarregar. Clicar numa fonte externa navega ao site correspondente.

## Validação e limites

Verificação de build TypeScript/Vite e testes em Chromium: oito seções, sete categorias, pesquisa com acentos, filtros combinados, ausência de resultados, limpeza, detalhes jurídicos, cinco explicações, cinco guias completos, controles/reset, foco do painel e layout em 320/390 px com fonte até 140%. Testes adicionais verificam a abertura GSAP, o desligamento do movimento e as cores principais de texto.

Esses testes não constituem auditoria WCAG 2.2 AA. Ainda é necessária avaliação com leitores de tela e pessoas com diferentes necessidades. A referência ERA Residence não pôde ser consultada no desenvolvimento inicial; a experiência existente foi preservada sem afirmar análise do site externo.

## Roteiro de vídeo (3 a 5 minutos)

- **30 s:** apresente ELO e o caráter acadêmico não oficial.
- **60 s:** escolha uma categoria; pesquise “BPC”, abra a referência e mostre resumo, alerta de revisão e fonte oficial.
- **45 s:** abra uma dúvida de matrícula ou negativa de plano e mostre os passos gerais.
- **45 s:** percorra as etapas do guia e os canais de orientação.
- **60 s:** demonstre teclado, fonte, contraste, tema e poucos estímulos; restaure preferências.
- **30 s:** apresente a comissão e o encerramento.
