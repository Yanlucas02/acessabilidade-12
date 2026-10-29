# SEM BARREIRAS

Protótipo acadêmico sobre inclusão digital e acessibilidade, em React, TypeScript, Vite, Tailwind CSS, GSAP/ScrollTrigger e Lucide React. Não utiliza backend, autenticação ou integrações externas.

## Executar

Requer Node.js 22.12+ (validado com Node 24) e npm.

```sh
npm ci
npm run dev
```

Para verificar e gerar a versão de produção: `npm run build`. Para servir essa versão: `npm run preview`.

## Jornada de apresentação (3 a 5 minutos)

1. Explore a abertura e o manifesto sobre barreiras digitais.
2. Em “Do seu jeito”, ajuste fonte, contraste, tema, leitura e movimentos. Os controles também estão no botão Acessibilidade do cabeçalho.
3. Explore VER, ENTENDER e NAVEGAR. As abas aceitam setas, Home e End. Percorra a interface com Tab e Shift+Tab e ative botões com Enter ou Espaço.
4. Escolha um serviço, clique em “Quero participar”, use um nome fictício, selecione um assunto e conclua a simulação. Experimente outro caminho.
5. Termine com a mensagem sobre acessibilidade como direito.

Os dados do formulário existem apenas na memória da página. Recarregar restaura as preferências e limpa a simulação. O sistema respeita a preferência inicial de movimento reduzido; há controle manual adicional. A animação usa GSAP com limpeza de contexto e não bloqueia conteúdo ou navegação.

## Validação

Build TypeScript/Vite e testes funcionais em Chromium: ajuste de fonte, contraste, painel, formulário, confirmação, abas, leitura simplificada e navegação móvel. Isso não constitui uma auditoria completa WCAG: recomenda-se validar com leitores de tela e pessoas com diferentes necessidades antes de qualquer uso real.

A referência externa ERA Residence estava bloqueada pela política de rede durante o desenvolvimento. A composição foi criada a partir da direção de arte fornecida, sem copiar imagens, conteúdo ou identidade da referência.

O rodapé reserva espaço para os integrantes do grupo. A arte abstrata é feita em CSS, sem depender de imagens remotas.
