# ELO — Direitos, Respeito e Inclusão

Adaptação do protótipo SEM BARREIRAS para o tema acadêmico **4.3 — Inclusão Digital e Acessibilidade**, com foco em informação e direitos de pessoas autistas e suas famílias. Mantém React, TypeScript, Vite, Tailwind CSS, GSAP/ScrollTrigger, Lucide e a identidade editorial existente.

**Projeto acadêmico não oficial**, com referência temática à Comissão de Direito da Pessoa com Autismo da OAB/DF — Subseção Águas Claras. Não representa a OAB nem oferece atendimento jurídico. As informações jurídicas introdutórias e os encaminhamentos precisam de validação profissional antes de uso real. Não há leis, benefícios, contatos, parcerias ou serviços específicos apresentados como garantidos.

## Executar

Requer Node.js 22.12+ (validado com Node 24) e npm.

```sh
npm ci
npm run dev
```

No PowerShell, se a execução de npm.ps1 estiver bloqueada, use `npm.cmd ci` e `npm.cmd run dev`, sem alterar a política de scripts do Windows.

`npm run build` valida TypeScript e gera a versão de produção. `npm run preview` serve esse build.

## O que foi reaproveitado

Hero fullscreen, composição abstrata CSS, tipografia, paleta, layouts assimétricos, revelações GSAP, parallax, navegação por âncoras, menu móvel, abas com teclado e painel de preferências com contenção e restauração de foco. O fluxo anterior de inscrição fictícia foi adaptado para um guia de leitura, removendo os campos de dados pessoais conforme o novo briefing. Sem novas dependências.

## Roteiro de apresentação (3 a 5 minutos)

1. **Início e autismo (45 s):** apresente ELO, a proposta não oficial e a diversidade de experiências autistas.
2. **Direitos (45 s):** explore as cinco categorias. Nas abas, teste as setas, Home e End e explique os limites do conteúdo introdutório.
3. **Conscientização (30 s):** destaque neurodiversidade, inclusão escolar, participação, autonomia e combate ao preconceito.
4. **Acessibilidade (60 s):** aumente o texto, altere contraste e tema, simplifique os textos e ative poucos estímulos. Esse modo remove somente arte decorativa e desliga animações. Restaure as preferências. O painel também está no cabeçalho.
5. **Guia (60 s):** escolha um dos quatro assuntos, percorra as três etapas, volte e recomece. Não existe formulário, cadastro, coleta de dados pessoais ou envio de informações.
6. **Comissão e encerramento (30 s):** apresente a atuação descrita no briefing e a mensagem “Inclusão não é favor. É direito.”

## Acessibilidade e privacidade

Use Tab/Shift+Tab para navegar, Enter/Espaço para ativar controles e Escape para fechar o painel. O painel impede interação com o fundo e devolve o foco ao botão de abertura. O guia transfere o foco para o título da etapa após uma ação. O modo simplificado adapta textos educativos, de direitos, do guia e da comissão. Informações essenciais continuam disponíveis no modo de poucos estímulos.

A preferência inicial de movimento reduzido do sistema é respeitada. É possível ajustar movimento e estímulos manualmente. GSAP limpa suas animações ao desligar os efeitos. Preferências e etapa são mantidas apenas em memória e reiniciam ao recarregar. Não há backend, autenticação, persistência de dados ou integrações externas.

## Verificação

Build TypeScript/Vite e testes funcionais em Chromium devem cobrir as cinco abas, quatro guias completos, preferências/reset, foco do painel, navegação móvel e ausência de campos de dados pessoais. Isso não substitui auditoria WCAG 2.2 AA nem testes com leitores de tela e pessoas com diferentes necessidades.

A referência ERA Residence estava bloqueada pela política de rede no desenvolvimento inicial. A composição existente foi preservada sem afirmar análise do site externo. A arte é local em CSS. O rodapé reserva espaço para nomes dos integrantes do grupo.
