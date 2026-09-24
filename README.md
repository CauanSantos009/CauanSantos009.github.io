[cards_r_pidos_de_consulta_enfermagem_aps_pbh.html](https://github.com/user-attachments/files/32587328/cards_r_pidos_de_consulta_enfermagem_aps_pbh.html)[Uploading cards_<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Portfólio & Guia Rápido de Enfermagem APS - CS Betânia / PBH</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <style>
    .custom-scrollbar::-webkit-scrollbar {
      width: 6px;
      height: 6px;
    }
    .custom-scrollbar::-webkit-scrollbar-track {
      background: #f1f5f9;
    }
    .custom-scrollbar::-webkit-scrollbar-thumb {
      background: #cbd5e1;
      border-radius: 4px;
    }
    .custom-scrollbar::-webkit-scrollbar-thumb:hover {
      background: #94a3b8;
    }
  </style>
</head>
<body class="bg-slate-50 text-slate-800 min-h-screen flex flex-col font-sans">

  <!-- Top Header -->
  <header class="bg-teal-700 text-white shadow-md sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 py-3 flex flex-col md:flex-row md:items-center md:justify-between gap-3">
      <div class="flex items-center space-x-3">
        <div class="bg-white/10 p-2.5 rounded-lg border border-white/20 flex items-center gap-2">
          <i class="fa-solid fa-graduation-cap text-2xl text-amber-300"></i>
          <i class="fa-solid fa-user-nurse text-xl text-teal-200"></i>
        </div>
        <div>
          <h1 class="text-xl font-bold tracking-tight">Portfólio & Guia de Enfermagem APS</h1>
          <p class="text-xs text-teal-100 flex items-center gap-2 flex-wrap">
            <span><i class="fa-solid fa-location-dot text-amber-300"></i> CS Betânia / PBH</span>
            <span>•</span>
            <span><i class="fa-solid fa-laptop-code text-emerald-300"></i> Tecnologias de Cuidado & Saúde Digital</span>
          </p>
        </div>
      </div>

      <!-- Quick Search Bar -->
      <div class="relative w-full md:w-80">
        <input type="text" id="searchInput" placeholder="Buscar no portfólio, exames, vacinas, C1..." 
               class="w-full pl-9 pr-8 py-1.5 rounded-lg text-sm bg-teal-800/80 text-white placeholder-teal-200 border border-teal-600 focus:outline-none focus:ring-2 focus:ring-amber-400 focus:bg-teal-900 transition">
        <i class="fa-solid fa-magnifying-glass absolute left-3 top-2.5 text-teal-300 text-xs"></i>
        <button id="clearSearch" class="hidden absolute right-2.5 top-2 text-teal-300 hover:text-white text-xs">
          <i class="fa-solid fa-xmark"></i>
        </button>
      </div>
    </div>

    <!-- Navigation Tabs -->
    <nav class="bg-teal-800 text-teal-100 px-4 border-t border-teal-600/50 overflow-x-auto custom-scrollbar">
      <div class="max-w-7xl mx-auto flex space-x-1 py-1 text-sm font-medium whitespace-nowrap">
        <button onclick="switchTab('portfolio')" id="tab-portfolio" class="tab-btn active px-3 py-2 rounded-md hover:bg-teal-700/60 flex items-center gap-2 transition">
          <i class="fa-solid fa-book-bookmark text-amber-300"></i>
          <span>Portfólio 2 (CS Betânia)</span>
        </button>
        <button onclick="switchTab('exames')" id="tab-exames" class="tab-btn px-3 py-2 rounded-md hover:bg-teal-700/60 flex items-center gap-2 transition">
          <i class="fa-solid fa-vial-circle-check text-emerald-300"></i>
          <span>Exames Solicitados (PBH)</span>
        </button>
        <button onclick="switchTab('vacinacao')" id="tab-vacinacao" class="tab-btn px-3 py-2 rounded-md hover:bg-teal-700/60 flex items-center gap-2 transition">
          <i class="fa-solid fa-syringe text-amber-300"></i>
          <span>Calendário Vacinal 2026</span>
        </button>
        <button onclick="switchTab('indicadores')" id="tab-indicadores" class="tab-btn px-3 py-2 rounded-md hover:bg-teal-700/60 flex items-center gap-2 transition">
          <i class="fa-solid fa-chart-line text-amber-200"></i>
          <span>Indicadores APS (C1-C7)</span>
        </button>
        <button onclick="switchTab('prescricao')" id="tab-prescricao" class="tab-btn px-3 py-2 rounded-md hover:bg-teal-700/60 flex items-center gap-2 transition">
          <i class="fa-solid fa-pills text-cyan-300"></i>
          <span>Prescrição pelo Enfermeiro</span>
        </button>
        <button onclick="switchTab('codigos')" id="tab-codigos" class="tab-btn px-3 py-2 rounded-md hover:bg-teal-700/60 flex items-center gap-2 transition">
          <i class="fa-solid fa-code text-indigo-300"></i>
          <span>Consulta de Códigos</span>
        </button>
      </div>
    </nav>
  </header>

  <!-- Main Container -->
  <main class="max-w-7xl mx-auto px-4 py-6 flex-1 w-full">

    <!-- Sub-filters Bar -->
    <div id="filterBar" class="mb-5 flex flex-wrap items-center justify-between gap-3 bg-white p-3 rounded-xl border border-slate-200 shadow-sm">
      <div id="filterCategoryButtons" class="flex flex-wrap items-center gap-1.5 text-xs">
        <!-- Injected via JS -->
      </div>
      <div class="text-xs text-slate-500 font-medium flex items-center gap-1">
        <i class="fa-solid fa-filter text-teal-600"></i>
        <span id="resultsCount">Exibindo itens</span>
      </div>
    </div>

    <!-- TAB: PORTFÓLIO 2 -->
    <section id="section-portfolio" class="tab-content space-y-6">
      
      <!-- Portfolio Banner / Intro Card -->
      <div class="bg-gradient-to-r from-teal-900 via-teal-800 to-slate-800 rounded-2xl p-6 text-white shadow-lg border border-teal-700/50 relative overflow-hidden">
        <div class="absolute -right-10 -bottom-10 opacity-10 text-9xl text-white pointer-events-none">
          <i class="fa-solid fa-laptop-medical"></i>
        </div>
        <div class="relative z-10 space-y-3 max-w-4xl">
          <div class="flex flex-wrap items-center gap-2">
            <span class="bg-amber-400 text-slate-900 text-xs font-black px-3 py-1 rounded-full uppercase tracking-wider shadow-sm">
              <i class="fa-solid fa-star me-1"></i> Portfólio 2
            </span>
            <span class="bg-teal-700/80 text-teal-100 border border-teal-500/40 text-xs px-3 py-1 rounded-full">
              Estágio Curricular em Enfermagem APS • CS Betânia
            </span>
          </div>
          <h2 class="text-2xl md:text-3xl font-extrabold tracking-tight text-white">
            Do Desafio à Inovação: Criação de Tecnologias de Cuidado em Saúde Digital
          </h2>
          <p class="text-sm text-teal-100/90 leading-relaxed">
            Uma síntese reflexiva sobre a experiência prática vivenciada no Centro de Saúde Betânia, demonstrando como a Enfermagem pode liderar a transformação digital na Atenção Primária à Saúde criando ferramentas de apoio à decisão clínica e fortalecimento do vínculo terapêutico.
          </p>
        </div>
      </div>

      <!-- Portfolio Grid Cards -->
      <div class="grid grid-cols-1 md:grid-cols-2 gap-6" id="portfolioCardsContainer">

        <!-- Card 1: Contexto -->
        <div class="portfolio-card bg-white rounded-2xl border border-slate-200 shadow-sm hover:shadow-md transition overflow-hidden flex flex-col" data-section="Contexto" data-search="contexto nacional local centro de saude betania problematizacao atuacao enfermagem tecnologias leves leves-duras">
          <div class="p-4 bg-teal-800 text-white flex items-center justify-between">
            <div class="flex items-center space-x-2">
              <span class="w-7 h-7 rounded-lg bg-teal-600 flex items-center justify-center font-bold text-amber-300 text-sm">1</span>
              <h3 class="font-bold text-base">1. Contexto</h3>
            </div>
            <span class="text-xs bg-teal-900/60 text-teal-200 px-2.5 py-1 rounded-full border border-teal-700 me-1">Cenário & Problematização</span>
          </div>
          <div class="p-5 flex-1 space-y-4 text-xs text-slate-700 leading-relaxed">
            
            <div class="bg-slate-50 p-3.5 rounded-xl border border-slate-200">
              <h4 class="font-bold text-teal-900 text-sm mb-1 flex items-center gap-1.5">
                <i class="fa-solid fa-map-location-dot text-teal-600"></i> Contexto Nacional / Local
              </h4>
              <p>
                A Atenção Primária à Saúde (APS) brasileira vive um momento de transição digital, impulsionado pela Estratégia de Saúde Digital. No entanto, no nível local — como vivenciado na rotina do <strong>Centro de Saúde Betânia</strong> —, o acesso rápido à informação atualizada durante os atendimentos ainda é um desafio. Muitas vezes, os profissionais dependem de cartilhas físicas desatualizadas ou de buscas demoradas no sistema, o que quebra o fluxo da consulta e gera impaciência nos usuários.
              </p>
            </div>

            <div class="bg-amber-50/70 p-3.5 rounded-xl border border-amber-200">
              <h4 class="font-bold text-amber-900 text-sm mb-1 flex items-center gap-1.5">
                <i class="fa-solid fa-triangle-exclamation text-amber-600"></i> Problematização
              </h4>
              <p>
                Após o atendimento da criança de 15 meses com calendário vacinal atrasado (relatado no portfólio anterior), deparei-me com uma lacuna operacional: a dificuldade de acessar e cruzar rapidamente as informações sobre imunobiológicos atrasados para estruturar um plano de atualização de doses, tudo isso enquanto tentava manter o engajamento e a empatia com pais resistentes. O "tempo perdido" na busca por diretrizes técnicas quase comprometeu a construção do vínculo.
              </p>
            </div>

            <div class="bg-teal-50/60 p-3.5 rounded-xl border border-teal-200">
              <h4 class="font-bold text-teal-900 text-sm mb-1 flex items-center gap-1.5">
                <i class="fa-solid fa-user-nurse text-teal-700"></i> Atuação da Enfermagem
              </h4>
              <p>
                A enfermagem do futuro não deve ser apenas usuária de tecnologias criadas por terceiros, mas também protagonista no desenvolvimento de soluções. A atuação do enfermeiro contemporâneo exige o domínio da informática em saúde para criar <strong>"tecnologias leves-duras"</strong> (ferramentas e equipamentos) que apoiem as <strong>"tecnologias leves"</strong> (relacionamento e acolhimento), qualificando a educação em saúde e o raciocínio clínico no ponto de cuidado (<em>point-of-care</em>).
              </p>
            </div>

          </div>
        </div>

        <!-- Card 2: Evidências Científicas -->
        <div class="portfolio-card bg-white rounded-2xl border border-slate-200 shadow-sm hover:shadow-md transition overflow-hidden flex flex-col" data-section="Evidências Científicas" data-search="evidencias cientificas pniis mhealth apoio a decisao clinica health literacy alfabetizacao em saude fake news">
          <div class="p-4 bg-teal-800 text-white flex items-center justify-between">
            <div class="flex items-center space-x-2">
              <span class="w-7 h-7 rounded-lg bg-teal-600 flex items-center justify-center font-bold text-amber-300 text-sm">2</span>
              <h3 class="font-bold text-base">2. Evidências Científicas</h3>
            </div>
            <span class="text-xs bg-teal-900/60 text-teal-200 px-2.5 py-1 rounded-full border border-teal-700 me-1">Fundamentação</span>
          </div>
          <div class="p-5 flex-1 space-y-4 text-xs text-slate-700 leading-relaxed">
            
            <div class="bg-indigo-50/60 p-3.5 rounded-xl border border-indigo-200">
              <h4 class="font-bold text-indigo-950 text-sm mb-1 flex items-center gap-1.5">
                <i class="fa-solid fa-scroll text-indigo-600"></i> Protocolos e Diretrizes Clínicas
              </h4>
              <p>
                A <strong>Política Nacional de Informação e Informática em Saúde (PNIIS)</strong> preconiza a adoção de Tecnologias da Informação e Comunicação (TICs) para apoiar a tomada de decisão clínica e melhorar a qualidade da assistência prestada à população.
              </p>
            </div>

            <div class="bg-emerald-50/60 p-3.5 rounded-xl border border-emerald-200">
              <h4 class="font-bold text-emerald-950 text-sm mb-1 flex items-center gap-1.5">
                <i class="fa-solid fa-microscope text-emerald-600"></i> Evidências da Literatura (mHealth)
              </h4>
              <p>
                A literatura especializada em <strong>mHealth (saúde móvel)</strong> demonstra que o uso de Sistemas de Apoio à Decisão Clínica baseados em dispositivos móveis reduz erros de conduta, otimiza o tempo de consulta e empodera o profissional.
              </p>
              <p class="mt-2">
                Estudos evidenciam que ferramentas visuais e interativas ajudam a traduzir jargões técnicos para uma linguagem compreensível, melhorando a alfabetização em saúde (<em>health literacy</em>) do paciente e mitigando os efeitos da desinformação, como as <em>fake news</em> sobre vacinas.
              </p>
            </div>

          </div>
        </div>

        <!-- Card 3: Percepções do Estudante -->
        <div class="portfolio-card bg-white rounded-2xl border border-slate-200 shadow-sm hover:shadow-md transition overflow-hidden flex flex-col" data-section="Percepções do Estudante" data-search="aproximacao percepcoes do estudante visao de si inteligência artificial notebooklm agente de inovacao tocar toque fisico">
          <div class="p-4 bg-teal-800 text-white flex items-center justify-between">
            <div class="flex items-center space-x-2">
              <span class="w-7 h-7 rounded-lg bg-teal-600 flex items-center justify-center font-bold text-amber-300 text-sm">3</span>
              <h3 class="font-bold text-base">3. Aproximação / Percepções do Estudante</h3>
            </div>
            <span class="text-xs bg-teal-900/60 text-teal-200 px-2.5 py-1 rounded-full border border-teal-700 me-1">Identidade Profissional</span>
          </div>
          <div class="p-5 flex-1 space-y-4 text-xs text-slate-700 leading-relaxed">
            
            <div class="bg-cyan-50/70 p-4 rounded-xl border border-cyan-200 space-y-2">
              <h4 class="font-bold text-cyan-950 text-sm flex items-center gap-1.5">
                <i class="fa-solid fa-lightbulb text-cyan-600 me-1"></i> Visão de si e da Enfermagem diante da situação
              </h4>
              <p class="text-slate-700">
                A necessidade de resolver o problema de acesso à informação me impulsionou a explorar a inteligência artificial.
              </p>
              <p class="text-slate-700">
                Ao criar o "aplicativo" (os cards interativos no NotebookLM), percebi uma mudança na minha própria identidade profissional: passei de um estudante focado exclusivamente no cuidado direto para um <strong>solucionador de problemas e agente de inovação</strong>.
              </p>
              <div class="p-3 bg-white/80 rounded-lg border border-cyan-200 text-cyan-900 italic font-medium">
                "Senti que a enfermagem tem um potencial gigantesco e muitas vezes inexplorado para a área de tecnologia. Ver a solução que eu desenhei funcionando 'na palma da mão' me trouxe segurança clínica e provou que organizar a informação é tão terapêutico quanto o toque físico."
              </div>
            </div>

          </div>
        </div>

        <!-- Card 4: Reflexão Crítica -->
        <div class="portfolio-card bg-white rounded-2xl border border-slate-200 shadow-sm hover:shadow-md transition overflow-hidden flex flex-col" data-section="Reflexão Crítica" data-search="reflexao critica situacao saude digital contato humano escuta qualificada confianca recusa vacinal">
          <div class="p-4 bg-teal-800 text-white flex items-center justify-between">
            <div class="flex items-center space-x-2">
              <span class="w-7 h-7 rounded-lg bg-teal-600 flex items-center justify-center font-bold text-amber-300 text-sm">4</span>
              <h3 class="font-bold text-base">4. Reflexão Crítica</h3>
            </div>
            <span class="text-xs bg-teal-900/60 text-teal-200 px-2.5 py-1 rounded-full border border-teal-700 me-1">Tecnologia & Humanização</span>
          </div>
          <div class="p-5 flex-1 space-y-3 text-xs text-slate-700 leading-relaxed">
            
            <div class="bg-rose-50/60 p-4 rounded-xl border border-rose-200 space-y-2">
              <h4 class="font-bold text-rose-950 text-sm flex items-center gap-1.5">
                <i class="fa-solid fa-heart-pulse text-rose-600"></i> Reflexão crítica sobre a situação
              </h4>
              <p>
                A inserção da saúde digital transforma profundamente o cotidiano dos serviços e a dinâmica das consultas. A criação dessa ferramenta provou que a tecnologia, quando bem aplicada, não mecaniza nem substitui o contato humano; pelo contrário, <strong>ela o resgata</strong>.
              </p>
              <p>
                Ao ter as respostas técnicas prontas na tela do celular, eliminei a desorganização e a ansiedade da busca por dados. Isso me permitiu manter o contato visual contínuo com os pais, focar na escuta qualificada e construir a confiança necessária para reverter a recusa vacinal.
              </p>
              <div class="bg-white p-3 rounded-lg border border-rose-200 font-bold text-slate-800">
                <i class="fa-solid fa-quote-left text-rose-400 me-1"></i>
                A tecnologia assumiu o trabalho burocrático de compilar dados, deixando para mim a essência humana de cuidar e persuadir.
              </div>
            </div>

          </div>
        </div>

        <!-- Card 5: Proposições (Full width on md+) -->
        <div class="portfolio-card md:col-span-2 bg-white rounded-2xl border border-slate-200 shadow-sm hover:shadow-md transition overflow-hidden flex flex-col" data-section="Proposições" data-search="proposicoes o que foi feito qualidade do cuidado inteligencia artificial generativa oficinas capacitação mhealth equipe multiprofissional">
          <div class="p-4 bg-teal-800 text-white flex items-center justify-between">
            <div class="flex items-center space-x-2">
              <span class="w-7 h-7 rounded-lg bg-teal-600 flex items-center justify-center font-bold text-amber-300 text-sm">5</span>
              <h3 class="font-bold text-base">5. Proposições de Intervenção</h3>
            </div>
            <span class="text-xs bg-teal-900/60 text-teal-200 px-2.5 py-1 rounded-full border border-teal-700 me-1">Melhoria da Qualidade do Cuidado</span>
          </div>
          <div class="p-5 flex-1 space-y-4 text-xs text-slate-700 leading-relaxed">
            
            <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
              <div class="bg-slate-50 p-4 rounded-xl border border-slate-200 space-y-2">
                <h4 class="font-bold text-teal-900 text-sm flex items-center gap-1.5">
                  <i class="fa-solid fa-circle-check text-emerald-600"></i> O que foi / está sendo feito
                </h4>
                <p>
                  A criação dos <strong>cards interativos no NotebookLM</strong> demonstrou ser uma estratégia altamente resolutiva para o manejo rápido de esquemas de atualização vacinal e argumentação científica no ponto de atendimento do CS Betânia.
                </p>
              </div>

              <div class="bg-teal-50/70 p-4 rounded-xl border border-teal-200 space-y-2">
                <h4 class="font-bold text-teal-950 text-sm flex items-center gap-1.5">
                  <i class="fa-solid fa-bullseye text-amber-600"></i> Propostas para Melhoria Sistêmica
                </h4>
                <p>
                  Para melhorar a qualidade do cuidado de forma sistêmica na unidade, proponho a disseminação do uso de ferramentas de inteligência artificial generativa e o incentivo ao desenvolvimento de soluções <em>mHealth</em> simples pela própria equipe multiprofissional.
                </p>
              </div>
            </div>

            <div class="bg-amber-50/80 p-4 rounded-xl border border-amber-200 flex flex-col md:flex-row items-start md:items-center justify-between gap-3">
              <div class="space-y-1">
                <h4 class="font-bold text-amber-950 text-sm flex items-center gap-1.5">
                  <i class="fa-solid fa-users-gear text-amber-700"></i> Sugestão Prática: Oficinas de Capacitação Multiprofissional
                </h4>
                <p class="text-slate-700">
                  Realização de oficinas para que outros estudantes e profissionais aprendam a criar seus próprios materiais interativos de bolso (sobre hipertensão, diabetes, pré-natal, vacinas, etc.), descentralizando o conhecimento, empoderando a equipe e agilizando o atendimento territorial.
                </p>
              </div>
              <button onclick="copyToClipboard('Portfólio 2: Do Desafio à Inovação: Criação de Tecnologias de Cuidado em Saúde Digital')" class="shrink-0 bg-amber-400 hover:bg-amber-500 text-slate-900 font-bold px-4 py-2 rounded-xl shadow-sm text-xs transition flex items-center gap-1.5">
                <i class="fa-solid fa-copy"></i> Copiar Título
              </button>
            </div>

          </div>
        </div>

      </div>
    </section>

    <!-- TAB: EXAMES SOLICITADOS -->
    <section id="section-exames" class="tab-content hidden">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-5" id="examesCardsContainer">
        <!-- Injected via JS -->
      </div>
    </section>

    <!-- TAB: CALENDÁRIO VACINAL 2026 -->
    <section id="section-vacinacao" class="tab-content hidden">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-5" id="vacinacaoCardsContainer">
        <!-- Injected via JS -->
      </div>
    </section>

    <!-- TAB: INDICADORES APS -->
    <section id="section-indicadores" class="tab-content hidden">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-5" id="indicadoresCardsContainer">
        <!-- Injected via JS -->
      </div>
    </section>

    <!-- TAB: PRESCRIÇÃO MEDICAMENTOSA -->
    <section id="section-prescricao" class="tab-content hidden">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-5" id="prescricaoCardsContainer">
        <!-- Injected via JS -->
      </div>
    </section>

    <!-- TAB: CONSULTA RÁPIDA DE CÓDIGOS -->
    <section id="section-codigos" class="tab-content hidden">
      <div class="bg-white rounded-xl border border-slate-200 shadow-sm overflow-hidden">
        <div class="p-4 bg-slate-100 border-b border-slate-200 flex flex-col md:flex-row md:items-center justify-between gap-3">
          <div>
            <h3 class="font-bold text-slate-800 text-base">Tabela Unificada de Registro para Indicadores e Vacinas</h3>
            <p class="text-xs text-slate-500">Procedimentos SIGTAP, CBOs autorizados, CIDs-10, CIAP-2 e Códigos PNI para prontuário/e-SUS</p>
          </div>
          <div class="flex items-center gap-2">
            <select id="codeTypeFilter" onchange="filterCodesTable()" class="text-xs border border-slate-300 rounded-lg px-2.5 py-1.5 bg-white font-medium focus:ring-2 focus:ring-teal-500">
              <option value="ALL">Todos os Tipos</option>
              <option value="PROCEDIMENTO">Procedimentos (SIGTAP)</option>
              <option value="VACINA">Código de Vacina (PNI)</option>
              <option value="CID10">CID-10</option>
              <option value="CIAP2">CIAP-2</option>
            </select>
          </div>
        </div>
        <div class="overflow-x-auto custom-scrollbar">
          <table class="w-full text-left text-xs text-slate-700">
            <thead class="bg-slate-50 text-slate-600 font-semibold border-b border-slate-200 uppercase tracking-wider">
              <tr>
                <th class="p-3">Ref/Contexto</th>
                <th class="p-3">Tipo</th>
                <th class="p-3">Código</th>
                <th class="p-3">Descrição / Aplicação</th>
                <th class="p-3 text-right">Ação</th>
              </tr>
            </thead>
            <tbody id="codesTableBody" class="divide-y divide-slate-200">
              <!-- Injected via JS -->
            </tbody>
          </table>
        </div>
      </div>
    </section>

    <!-- Empty State -->
    <div id="emptyState" class="hidden text-center py-12 bg-white rounded-xl border border-slate-200 shadow-sm my-4">
      <div class="inline-flex items-center justify-center w-12 h-12 rounded-full bg-slate-100 text-slate-400 mb-3">
        <i class="fa-solid fa-magnifying-glass text-xl"></i>
      </div>
      <h3 class="text-base font-bold text-slate-700">Nenhum resultado encontrado</h3>
      <p class="text-xs text-slate-500 mt-1 max-w-md mx-auto">Tente ajustar seus termos de busca ou mude de aba para encontrar informações no portfólio, exames, vacinas ou indicadores.</p>
    </div>

  </main>

  <!-- Notification Toast -->
  <div id="toast" class="fixed bottom-4 right-4 bg-slate-900 text-white text-xs px-4 py-2.5 rounded-lg shadow-lg transform translate-y-16 opacity-0 transition-all duration-300 z-50 flex items-center gap-2">
    <i class="fa-solid fa-circle-check text-emerald-400"></i>
    <span id="toastMsg">Código copiado com sucesso!</span>
  </div>

  <!-- Detail Modal -->
  <div id="modalBackdrop" class="fixed inset-0 bg-slate-900/50 backdrop-blur-sm z-50 hidden opacity-0 transition-opacity duration-200 flex items-center justify-center p-4">
    <div class="bg-white rounded-2xl shadow-xl border border-slate-200 max-w-2xl w-full max-h-[90vh] flex flex-col overflow-hidden transform scale-95 transition-transform duration-200" id="modalContainer">
      <div class="p-4 bg-teal-700 text-white flex items-center justify-between" id="modalHeader">
        <h3 class="font-bold text-base flex items-center gap-2" id="modalTitle">
          <!-- Title -->
        </h3>
        <button onclick="closeModal()" class="text-white/80 hover:text-white p-1 rounded-lg transition">
          <i class="fa-solid fa-xmark text-lg"></i>
        </button>
      </div>
      <div class="p-5 overflow-y-auto custom-scrollbar text-sm space-y-4 flex-1" id="modalBody">
        <!-- Content -->
      </div>
      <div class="p-3 bg-slate-100 border-t border-slate-200 flex justify-end">
        <button onclick="closeModal()" class="px-4 py-1.5 bg-slate-200 hover:bg-slate-300 text-slate-700 font-medium text-xs rounded-lg transition">
          Fechar
        </button>
      </div>
    </div>
  </div>

  <!-- Footer -->
  <footer class="bg-white border-t border-slate-200 py-4 text-center text-xs text-slate-500 mt-auto">
    <div class="max-w-7xl mx-auto px-4 flex flex-col sm:flex-row items-center justify-between gap-2">
      <p>© Portfólio de Estágio APS - CS Betânia / PBH • Enfermagem & Saúde Digital (2026)</p>
      <div class="flex items-center space-x-3 text-slate-400">
        <span title="Regimento Interno da Enfermagem APS"><i class="fa-solid fa-shield-halved"></i> CS Betânia</span>
        <span>•</span>
        <span title="Exames da Enfermagem"><i class="fa-solid fa-vial"></i> Exames PBH</span>
      </div>
    </div>
  </footer>

  <script>

    const DATA_EXAMES_PBH = [
      {
        id: "EX_01",
        categoria: "Pré-Natal / Hematologia",
        nome: "ABO / Rh / Factor DU",
        indicacoes: "Gestantes no início do pré-natal (1ª consulta) ou recém-nascidos/usuários em investigação hemolítica.",
        finalidade: "Determinar a tipagem sanguínea e o fator Rh (incluindo pesquisa do fator Rh fraco - D fraco/DU) para prevenir a Doença Hemolítica do Recém-Nascido (eritroblastose fetal) e planejar a imunoglobulina anti-D na gestante Rh negativo.",
        orientacoes: "Solicitar no 1º trimestre da gestação. Se gestante Rh negativo e parceiro Rh positivo ou desconhecido, realizar Teste de Coombs Indireto."
      },
      {
        id: "EX_02",
        categoria: "Infectologia / Respiratório",
        nome: "BAAR (Bacterioscopia) e TRM-TB (Teste Rápido Molecular para Tuberculose)",
        indicacoes: "Sintomáticos respiratórios (tosse por 3 semanas ou mais), suspeita de tuberculose pulmonar ou acompanhamento do tratamento da TB.",
        finalidade: "Identificação direta de Bacilos Álcool-Ácido Resistentes no escarro (BAAR) e detecção molecular do DNA do Mycobacterium tuberculosis com pesquisa de resistência à rifampicina (TRM-TB).",
        orientacoes: "TRM-TB é indicado prioritariamente para diagnóstico inicial. Coletar 2 amostras de escarro (1ª no momento da consulta e 2ª na manhã seguinte ao despertar)."
      },
      {
        id: "EX_03",
        categoria: "Saúde da Mulher / Planejamento",
        nome: "BHCG (Gonadotrofina Coriônica Humana - Fração Beta)",
        indicacoes: "Atraso menstrual, suspeita clínica de gestação, diagnóstico confirmatório para início do pré-natal.",
        finalidade: "Confirmar ou descartar a gravidez por meio da dosagem hormonal no sangue ou urina.",
        orientacoes: "Utilizado para captação precoce da gestante no 1º trimestre da gestação, permitindo início imediato do acompanhamento pré-natal."
      },
      {
        id: "EX_04",
        categoria: "Saúde da Mulher / Rastreamento",
        nome: "Citopatológico do Colo Uterino (Papanicolau)",
        indicacoes: "Mulheres sexualmente ativas ou com história de atividade sexual, prioritariamente na faixa etária de 25 a 64 anos.",
        finalidade: "Rastreamento e detecção precoce de lesões pré-neoplásicas (displasias) e do Câncer de Colo do Útero (infecção persistente por HPV).",
        orientacoes: "Realizar anualmente; após 2 exames normais consecutivos, realizar a cada 3 anos. Se alterado (ASC-US, LSIL, HSIL), encaminhar segundo o protocolo da PBH."
      },
      {
        id: "EX_05",
        categoria: "Condições Crônicas / Risco CV",
        nome: "Colesterol (Frações - HDL / LDL / VLDL)",
        indicacoes: "Adultos > 35 anos (homens) e > 45 anos (mulheres), hipertensos, diabéticos, obesos ou com histórico familiar de aterosclerose/risco CV.",
        finalidade: "Avaliação do perfil lipídico quantitativo para estadiamento do risco cardiovascular, prevenção de eventos coronarianos e acompanhamento do tratamento de dislipidemias.",
        orientacoes: "Jejum recomendado segundo instrução do laboratório local da PBH. Calcular o risco cardiovascular global na consulta."
      },
      {
        id: "EX_06",
        categoria: "Condições Crônicas / Risco CV",
        nome: "Colesterol Total",
        indicacoes: "Rastreamento inicial de alteração no metabolismo dos lipídios em adultos na APS.",
        finalidade: "Mensurar a concentração total de colesterol circulante no sangue para triagem de dislipidemia.",
        orientacoes: "Geralmente dosado em conjunto com as frações (HDL/LDL) e triglicérides para formar o painel lipídico completo."
      },
      {
        id: "EX_07",
        categoria: "Renal / Condições Crônicas",
        nome: "Creatinina Sérica",
        indicacoes: "Hipertensos, diabéticos, idosos, usuários em uso prolongado de medicamentos nefrotóxicos ou com suspeita de Doença Renal Crônica (DRC).",
        finalidade: "Avaliar a função renal e estimar a Taxa de Filtração Glomerular (eTFG) para rastreamento e estadiamento de nefropatias.",
        orientacoes: "Utilizar o valor para calcular a TFGe (CKD-EPI) no e-SUS e direcionar conduta na linha de cuidado de HAS/DM."
      },
      {
        id: "EX_08",
        categoria: "Geral / Microbiologia",
        nome: "Cultura de Feridas (com Antibiograma)",
        indicacoes: "Lesões/úlceras crônicas com sinais clínicos de infecção local (exsudato purulento, hiperemia acentuada, odor, calor, retardo na cicatrização).",
        finalidade: "Isolar e identificar a bactéria causadora da infecção cutânea e determinar sua sensibilidade aos antimicrobianos (antibiograma).",
        orientacoes: "Coletar o aspirado ou swab da lesão APÓS limpeza abundante da ferida com soro fisiológico 0,9%, conforme o Protocolo de Feridas da PBH."
      },
      {
        id: "EX_09",
        categoria: "Cardiovascular / Geral",
        nome: "Eletrocardiograma (ECG)",
        indicacoes: "Usuários hipertensos, diabéticos, idosos, avaliação pré-operatória, precordialgia atípica ou acompanhamento de arritmias.",
        finalidade: "Identificar distúrbios de condução elétrica, arritmias cardíacas, sinais de sobrecarga ventricular e alterações isquêmicas (IAM/isquemia silenciosa).",
        orientacoes: "Realizado via TeleCardiologia/Telessaúde no próprio Centro de Saúde da PBH com laudo rápido fornecido por especialistas."
      },
      {
        id: "EX_10",
        categoria: "Hematologia / Pré-Natal",
        nome: "Eletroforese de Hemoglobina B",
        indicacoes: "Gestantes no pré-natal, triagem de hemoglobinopatias em indivíduos com anemia crônica ou histórico familiar de Doença Falciforme.",
        finalidade: "Identificar variações e mutações nas cadeias de hemoglobina (HbA, HbS, HbC, traço falciforme) para diagnóstico de Anemia Falciforme e Talassemias.",
        orientacoes: "Exame fundamental no pré-natal para identificação de casais com traço falcêmico e aconselhamento genético."
      },
      {
        id: "EX_11",
        categoria: "Gastroenterologia / Parasitologia",
        nome: "Exame Parasitológico de Fezes (EPF)",
        indicacoes: "Crianças e adultos com sintomas gastrointestinais (diarreia, dor abdominal, prurido anal), anemia sem causa aparente ou desnutrição.",
        finalidade: "Detectar a presença de ovos, cistos, larvas ou trofozoítos de helmintos e protozoários intestinais.",
        orientacoes: "Coletar amostra única ou 3 amostras em dias alternados (segundo o frasco/conservante fornecido pelo laboratório)."
      },
      {
        id: "EX_12",
        categoria: "Saúde do Homem / Planejamento",
        nome: "Espermograma pós-Vasectomia",
        indicacoes: "Homens submetidos ao procedimento cirúrgico de vasectomia como método contraceptivo definitivo.",
        finalidade: "Confirmar a ausência total de espermatozoides (azoospermia) no sêmen para validação do sucesso do planejamento familiar.",
        orientacoes: "Realizado após aproximadamente 60 a 90 dias do procedimento (ou após 20 ejaculações). Orientar manutenção de método barreira até o resultado confirmatório."
      },
      {
        id: "EX_13",
        categoria: "Urologia / Rotina",
        nome: "Exame de Urina Rotina (EAS / Elementos Anormais e Sedimentoscopia)",
        indicacoes: "Suspeita de Infecção do Trato Urinário (ITU), acompanhamento de gestantes, hipertensos, diabéticos e investigação de hematúria/proteinúria.",
        finalidade: "Avaliar parâmetros físicos e químicos (pH, densidade, proteína, glicose, leucócitos, nitrito, hemácias) e sedimento urinário.",
        orientacoes: "Orientar higiene íntima prévia e coleta da amostra do 1º jato desprezado (jato médio da primeira urina da manhã)."
      },
      {
        id: "EX_14",
        categoria: "Endocrinologia / Rastreamento",
        nome: "Glicemia de Jejum",
        indicacoes: "Rastreamento e diagnóstico de Diabetes Mellitus (DM2) e Pré-Diabetes em adultos, gestantes no 1º trimestre e acompanhamento de rotina.",
        finalidade: "Dosar a concentração de glicose plasmática após jejum calórico para triagem metabólica.",
        orientacoes: "Jejum necessário de 8 a 12 horas. Se resultado ≥ 126 mg/dL em duas ocasiões, confirma o diagnóstico de Diabetes."
      },
      {
        id: "EX_15",
        categoria: "Endocrinologia / Diabetes",
        nome: "Glicohemoglobina (Hemoglobina Glicada - HbA1c)",
        indicacoes: "Monitoramento do controle glicêmico de usuários já diagnosticados com Diabetes Mellitus tipo 1 ou 2 e confirmação diagnóstica.",
        finalidade: "Avaliar a média da glicemia do paciente nos últimos 2 a 3 meses (vida média das hemácias), prevenindo complicações micro e macrovasculares.",
        orientacoes: "Solicitar a cada 6 meses em diabéticos compensados ou a cada 3 meses se descompensados. Meta geral: HbA1c < 7,0%."
      },
      {
        id: "EX_16",
        categoria: "Endocrinologia / Diabetes",
        nome: "Glicose Pós-Prandial",
        indicacoes: "Avaliação do controle metabólico glicêmico em pacientes diabéticos ou com glicemia de jejum alterada.",
        finalidade: "Mensurar os picos de glicemia sanguínea duas horas após uma refeição habitual para avaliar a resposta insulínica pós-prandial.",
        orientacoes: "Coletar o sangue exatamente 2 horas após o início do almoço ou refeição estipulada."
      },
      {
        id: "EX_17",
        categoria: "Hematologia / Geral",
        nome: "Hemograma Completo",
        indicacoes: "Avaliação de quadros anêmicos, processos infecciosos/inflamatórios, febre a esclarecer, pré-natal, contagem de plaquetas em dengue.",
        finalidade: "Avaliar a série vermelha (eritrócitos, hemoglobina, hematócrito), série branca (leucograma para infecções) e plaquetograma (coagulação).",
        orientacoes: "Solicitado de rotina na 1ª consulta de pré-natal, 3º trimestre da gestação e na investigação de fadiga/sangramentos."
      },
      {
        id: "EX_18",
        categoria: "Saúde da Mulher / Rastreamento",
        nome: "Mamografia (MMG Bilateral)",
        indicacoes: "Rastreamento quadrienal/bianual em mulheres de 50 a 69 anos de idade, ou em faixas etárias específicas sob recomendação clínica.",
        finalidade: "Rastreamento e detecção precoce do Câncer de Mama por meio de radiografia das mamas (identificação de microcalcificações e nódulos subclínicos).",
        orientacoes: "Classificação BI-RADS: Se BI-RADS 1 e 2 (normal), repetir a cada 2 anos. BI-RADS 0, 3, 4 ou 5 seguir fluxo de encaminhamento rápido da PBH."
      },
      {
        id: "EX_19",
        categoria: "Renal / Diabetes",
        nome: "Microalbuminúria Isolada",
        indicacoes: "Pacientes diabéticos e hipertensos para rastreamento de lesão renal incipiente.",
        finalidade: "Detectar pequenas quantidades de albumina na urina antes que sejam detectáveis no exame de urina de rotina (EAS).",
        orientacoes: "Indicador precoce de nefropatia diabética e risco cardiovascular aumentado. Preferencialmente dosada junto com a creatinina urinária."
      },
      {
        id: "EX_20",
        categoria: "Renal / Diabetes",
        nome: "Relação Albumina / Creatinina Urinária (RAC)",
        indicacoes: "Rastreamento anual obrigatório de Doença Renal Crônica em pessoas com Diabetes Mellitus e Hipertensão na APS.",
        finalidade: "Avaliar a excreção urinária de albumina corrigida pela creatinina em amostra isolada de urina, dispensando a coleta trabalhosa de urina de 24 horas.",
        orientacoes: "Valores entre 30 e 300 mg/g indicam microalbuminúria (nefropatia incipiente) e > 300 mg/g indicam macroalbuminúria."
      },
      {
        id: "EX_21",
        categoria: "Eletrólitos / Cardio-Renal",
        nome: "Dosagem de Potássio (K+)",
        indicacoes: "Acompanhamento de hipertensos em uso de diuréticos, IECA/BRA, usuários com DRC ou arritmias.",
        finalidade: "Avaliar o equilíbrio eletrolítico plasmático e prevenir complicações de hipocalemia ou hipercalemia (risco de parada cardíaca/arritmias).",
        orientacoes: "Solicitar em conjunto com a dosagem de Sódio e Creatinina ao ajustar anti-hipertensivos."
      },
      {
        id: "EX_22",
        categoria: "Eletrólitos / Cardio-Renal",
        nome: "Dosagem de Sódio (Na+)",
        indicacoes: "Idosos, pacientes em uso de psicotrópicos/diuréticos, quadros de desidratação grave ou alteração do estado mental.",
        finalidade: "Avaliar o equilíbrio hidroeletrolítico e osmolaridade plasmática (identificação de hiponatremia/hipernatremia).",
        orientacoes: "Coleta sanguínea de rotina no acompanhamento de idosos frágeis e usuários de diuréticos tiazídicos."
      },
      {
        id: "EX_23",
        categoria: "Infectologia / Sorologias",
        nome: "Sorologias (VDRL/FTA-ABS, Anti-HIV, Anti-HCV, HBsAg, Anti-HBs, Anti-HBc)",
        indicacoes: "Pré-natal (1º e 3º trimestres), rastreamento de ISTs, exposições de risco, acidentes com material biológico e acompanhamento geral.",
        finalidade: "VDRL/FTA-ABS (Sífilis), Anti-HIV (AIDS), Anti-HCV (Hepatite C), HBsAg/Anti-HBs/Anti-HBc (Infecção ativa, imunidade ou contato prévio com Hepatite B).",
        orientacoes: "Podem ser complementados ou precedidos pelos Testes Rápidos nas Unidades Básicas de Saúde para início imediato do cuidado."
      },
      {
        id: "EX_24",
        categoria: "Endocrinologia / Gestação",
        nome: "Teste de Tolerância Oral à Glicose (TOTG 75g)",
        indicacoes: "Gestantes entre a 24ª e 28ª semana de gestação (rastreamento de Diabetes Gestacional - DMG) e investigação de DM em adultos com jejum alterado.",
        finalidade: "Diagnosticar o Diabetes Mellitus Gestacional ou intolerância à glicose através da dosagem da glicemia em jejum, 1 hora e 2 horas após sobrecarga de 75g de glicose.",
        orientacoes: "Critérios DMG: Jejum ≥ 92 mg/dL, 1h ≥ 180 mg/dL ou 2h ≥ 153 mg/dL (apenas 1 valor alterado confirma DMG)."
      },
      {
        id: "EX_25",
        categoria: "Infectologia / Testes Rápidos",
        nome: "Testes Rápidos (Anti-HIV, Treponêmico-Sífilis, Anti-HCV, HBsAg, Gravidez)",
        indicacoes: "Acolhimento na APS, pré-natal, parceiros sexuais, populações chave, violência sexual e confirmação de gestação.",
        finalidade: "Diagnóstico presuntivo/definitivo em até 30 minutos na própria unidade de saúde, permitindo conduta terapêutica e encaminhamento imediato.",
        orientacoes: "Em caso de Teste Rápido de Sífilis positivo em gestante, iniciar o tratamento com Penicilina Benzatina imediatamente na UBS."
      },
      {
        id: "EX_26",
        categoria: "Infectologia / Pré-Natal",
        nome: "Toxoplasmose (Coleta em Papel Filtro)",
        indicacoes: "Triagem neonatal ou rastreamento em locais específicos conforme diretriz do programa de triagem.",
        finalidade: "Rastreamento sorológico prático para detecção de infecção por Toxoplasma gondii.",
        orientacoes: "Amostra obtida por punção capilar e seca em papel filtro para envio ao laboratório de referência."
      },
      {
        id: "EX_27",
        categoria: "Infectologia / Pré-Natal",
        nome: "Toxoplasmose IgG / IgM (Sérica)",
        indicacoes: "Gestantes no 1º trimestre do pré-natal para verificação de imunidade ou infecção aguda.",
        finalidade: "Identificar suscetibilidade (IgG- e IgM-), imunidade prévia (IgG+ e IgM-) ou infecção aguda recente (IgM+ e IgG+ ou -), que exige conduta para prevenir a Toxoplasmose Congênita.",
        orientacoes: "Se IgM+ e IgG+, solicitar Teste de Avidez de IgG (se gestação < 16 semanas) e encaminhar imediatamente para o pré-natal de alto risco."
      },
      {
        id: "EX_28",
        categoria: "Condições Crônicas / Risco CV",
        nome: "Triglicérides",
        indicacoes: "Avaliação do perfil metabólico e de risco cardiovascular em hipertensos, diabéticos, obesos ou etilistas.",
        finalidade: "Mensurar a concentração de triglicerídeos no sangue para rastreamento de hipertrigliceridemia e prevenção de pancreatite aguda (se > 500 mg/dL).",
        orientacoes: "Parte integrante do perfil lipídico. Exige jejum de 12 horas para maior precisão analítica."
      },
      {
        id: "EX_29",
        categoria: "Endocrinologia / Rastreamento",
        nome: "TSH (Hormônio Tireoestimulante)",
        indicacoes: "Gestantes na 1ª consulta pré-natal, idosos, investigação de bócio, fadiga crônica, alterações de peso inexplicadas ou dislipidemia.",
        finalidade: "Avaliar a função da glândula tireoide para diagnóstico de Hipotireoidismo ou Hipertireoidismo primário.",
        orientacoes: "No pré-natal, o hipotireoidismo não tratado associa-se a déficit neuropsicológico fetal e abortamento."
      },
      {
        id: "EX_30",
        categoria: "Saúde da Mulher / Ultrassonografia",
        nome: "Ultrassom Endovaginal (Pélvico Transvaginal)",
        indicacoes: "Avaliação de dor pélvica, sangramento uterino anormal, suspeita de cistos ovarianos, miomas ou confirmação de gestação inicial.",
        finalidade: "Visualização detalhada por imagem da anatomia do útero, ovários e endométrio, além da confirmação de gravidez tópica inicial e batimentos cardíacos fetais.",
        orientacoes: "Exame complementar solicitado conforme diretrizes e protocolos da saúde da mulher da PBH."
      },
      {
        id: "EX_31",
        categoria: "Saúde da Mulher / Pré-Natal",
        nome: "Ultrassom Obstétrico",
        indicacoes: "Gestantes no acompanhamento pré-natal para avaliação do desenvolvimento e vitalidade fetal.",
        finalidade: "Determinar a idade gestacional exata, estimar peso fetal, avaliar placenta, líquido amniótico e anatomia do bebê.",
        orientacoes: "Idealmente realizar a USG obstétrica precoce no 1º trimestre (para datar a gestação) e USG morfológica conforme disponibilidade do sistema."
      }
    ];

    const DATA_VACINAS_2026 = [
      {
        id: "VAC_BCG",
        ciclo: "Criança",
        vacina: "Vacina BCG (Atenuada)",
        protecao: "Formas graves de tuberculose (miliar e meníngea) e complicações.",
        composicao: "Bacilos vivos atenuados (Mycobacterium bovis).",
        viaVol: "Intradérmica (ID) - RN até 11m29d: 0,05 mL | A partir de 1 ano: 0,1 mL.",
        esquema: "Dose única ao nascer, ainda na maternidade ou na 1ª visita ao serviço de saúde (até 4a11m29d).",
        reforco: "Não há reforço de rotina.",
        intervalo: "Dose única.",
        particularidades: "Em recém-nascidos com peso < 2 kg, adiar até atingir 2 kg. Crianças expostas ao HIV não vacinadas podem receber se assintomáticas e sem sinais de imunodepressão.",
        contraindicacoes: "Contraindicada em imunodeficiências primárias ou adquiridas, lesões graves de pele no local, ou em uso de imunossupressores/corticosteroides em alta dose."
      },
      {
        id: "VAC_PENTA",
        ciclo: "Criança",
        vacina: "Vacina Penta (DTP/HepB/Hib)",
        protecao: "Difteria, Tétano, Coqueluche, Hepatite B, infecções por Haemophilus influenzae b.",
        composicao: "Toxoides diftérico/tetânico, B. pertussis inativada, HBsAg e oligossacarídeos conjugados de Hib.",
        viaVol: "Intramuscular (IM) - 0,5 mL.",
        esquema: "3 doses (2 meses, 4 meses e 6 meses de idade).",
        reforco: "Reforços com DTP aos 15 meses e aos 4 anos de idade.",
        intervalo: "Recomendado: 60 dias entre doses. Mínimo: 30 dias. Idade mínima: 6 semanas.",
        particularidades: "Se a criança não recebeu a dose de Hepatite B nas primeiras 30 dias de vida, observar intervalo de pelo menos 4 meses entre a 1ª e a 3ª dose considerando o componente HepB.",
        contraindicacoes: "Encefalopatia nos 7 dias após dose anterior. Anafilaxia aos componentes."
      },
      {
        id: "VAC_VIP",
        ciclo: "Criança",
        vacina: "Vacina Poliomielite Inativada (VIP)",
        protecao: "Poliomielite (paralisia infantil) causadas pelos poliovírus tipos 1, 2 e 3.",
        composicao: "Vírus inativados dos tipos 1, 2 e 3.",
        viaVol: "Intramuscular (IM) - 0,5 mL.",
        esquema: "3 doses (2 meses, 4 meses e 6 meses de idade).",
        reforco: "1 dose de reforço aos 15 meses de idade.",
        intervalo: "Entre doses do esquema: Recomendado 60 dias (mínimo 30 dias). Reforço: 9 meses após a 3ª dose (mínimo 6 meses).",
        particularidades: "Substitui completamente a VOP (oral) para maior segurança contra eventos adversos associados ao vírus vacinal atenuado.",
        contraindicacoes: "Reação anafilática comprovada a doses anteriores."
      },
      {
        id: "VAC_VORH",
        ciclo: "Criança",
        vacina: "Vacina Rotavírus Humano (VORH)",
        protecao: "Gastroenterite viral por rotavírus sorogrupo G1 e complicações.",
        composicao: "Vírus vivos atenuados G1P[8].",
        viaVol: "Via Oral (VO) - 1,5 mL (administrar todo o conteúdo da bisnaga).",
        esquema: "2 doses (2 meses e 4 meses de idade).",
        reforco: "Não há reforço.",
        intervalo: "Recomendado: 60 dias. Mínimo: 30 dias.",
        particularidades: "ATENÇÃO RÍGIDA AO PRAZO: 1ª dose pode ser feita de 1m15d até 11m29d. Caso a 1ª dose NÃO seja realizada dentro do intervalo preconizado, a criança PERDERÁ a oportunidade da vacina.",
        contraindicacoes: "Invaginação intestinal prévia, malformação congênita não corrigida do trato digestivo, imunodeficiência grave."
      },
      {
        id: "VAC_SCR",
        ciclo: "Criança",
        vacina: "Tríplice Viral (SCR - Sarampo, Caxumba, Rubéola)",
        protecao: "Sarampo, Caxumba, Rubéola e suas complicações.",
        composicao: "Vírus vivos atenuados de Sarampo, Caxumba e Rubéola.",
        viaVol: "Subcutânea (SC) - 0,5 mL.",
        esquema: "2 doses: 1ª dose aos 12 meses e 2ª dose aos 15 meses (com a vacina Varicela/Tetraviral).",
        reforco: "Profissionais de saúde e viajantes podem necessitar resgate.",
        intervalo: "Recomendado: 30 dias entre doses. Mínimo: 15 dias (situações de bloqueio/epidemia).",
        particularidades: "NÃO UTILIZAR a vacina SCR do laboratório Serum Institute of India para pessoas com história de ALERGIA GRAVE À PROTEÍNA DO LEITE DE VACA (lactoalbumina). Intolerantes à lactose podem receber.",
        contraindicacoes: "Gestantes, imunodeprimidos graves e anafilaxia prévia ao ovo de galinha/componentes."
      },
      {
        id: "VAC_HPV4_ADOLESC",
        ciclo: "Adolescente / Jovem",
        vacina: "Vacina HPV Quadrivalente (HPV4)",
        protecao: "Câncer de colo do útero, vulva, vagina, ânus, pênis, orofaringe e verrugas anogenitais (sorotipos 6, 11, 16, 18).",
        composicao: "Antígenos recombinantes da proteína L1 do HPV.",
        viaVol: "Intramuscular (IM) - 0,5 mL.",
        esquema: "DOSE ÚNICA para meninas e meninos de 9 a 14 anos 11 meses e 29 dias.",
        reforco: "Estratégia de resgate: 1 dose única na faixa de 15 a 19 anos sem histórico vacinal.",
        intervalo: "Dose única.",
        particularidades: "Também indicada para imunocomprometidos (HIV, transplantados, doentes oncólogicos) de 9 a 45 anos em esquema de 3 doses (0, 2, 6 meses).",
        contraindicacoes: "Gestantes (se vacinada inadvertidamente, interromper o esquema e completar pós-parto)."
      },
      {
        id: "VAC_DENGUE",
        ciclo: "Adolescente / Jovem",
        vacina: "Vacina Dengue (Atenuada - Qdenga)",
        protecao: "Dengue por qualquer um dos 4 sorotipos (DEN-1, DEN-2, DEN-3 e DEN-4).",
        composicao: "Vírus vivos atenuados quiméricos da dengue.",
        viaVol: "Subcutânea (SC) - 0,5 mL.",
        esquema: "2 doses com intervalo de 3 meses entre D1 e D2.",
        reforco: "Não há recomendação de reforço no momento.",
        intervalo: "3 meses entre D1 e D2.",
        particularidades: "Público alvo de 10 a 14 anos. Após infecção por dengue, aguardar 6 meses para iniciar vacinação.",
        contraindicacoes: "Gestantes, lactantes, imunodeficiências primárias/adquiridas."
      },
      {
        id: "VAC_DTPA_GESTANTE",
        ciclo: "Gestante",
        vacina: "Vacina dTpa (Tríplice Bacteriana Acelular)",
        protecao: "Difteria, Tétano e Coqueluche do recém-nascido via passagem transplacentária de anticorpos.",
        composicao: "Toxoides diftérico, tetânico e componentes acelulares da B. pertussis.",
        viaVol: "Intramuscular (IM) - 0,5 mL.",
        esquema: "1 DOSE A CADA GESTAÇÃO, a partir da 20ª semana gestacional.",
        reforco: "Se a gestante perdeu a oportunidade na gravidez, administrar no puerpério imediato (até 45 dias pós-parto).",
        intervalo: "Mínimo de 60 dias de qualquer dose anterior contendo componente tetânico.",
        particularidades: "Fundamental para imunizar o bebê prematuro/lactente jovem contra a coqueluche grave.",
        contraindicacoes: "Encefalopatia nos 7 dias posteriores a dose anterior."
      },
      {
        id: "VAC_VSR_GESTANTE",
        ciclo: "Gestante",
        vacina: "Vacina Vírus Sincicial Respiratório (VVSR Recombinante)",
        protecao: "Infecções do trato respiratório inferior (bronquiolite grave) por VSR subgrupos A e B em bebês até 6 meses.",
        composicao: "Glicoproteína F do VSR A e B produzida por DNA recombinante.",
        viaVol: "Intramuscular (IM) - 0,5 mL.",
        esquema: "1 DOSE A CADA GESTAÇÃO, a partir da 28ª semana de gestação.",
        reforco: "Aplicar a cada nova gestação.",
        intervalo: "Dose única por gestação a partir da 28ª semana.",
        particularidades: "Proteção passiva essencial nos primeiros meses de vida do bebê.",
        contraindicacoes: "Hipersensibilidade grave conhecida a qualquer componente."
      },
      {
        id: "VAC_FLU_IDOSO",
        ciclo: "Idoso / Adulto",
        vacina: "Vacina Influenza Trivalente (INF3)",
        protecao: "Gripe por vírus Myxovirus influenzae e suas complicações respiratórias/cardíacas.",
        composicao: "Vírus inativados fracionados da temporada.",
        viaVol: "Intramuscular (IM) ou Subcutânea (SC) - 0,5 mL.",
        esquema: "1 DOSE ANUAL na campanha de vacinação nacional.",
        reforco: "Anual.",
        intervalo: "Anual.",
        particularidades: "Indicada para gestantes, idosos (≥ 60 anos), comorbidades e profissionais de saúde.",
        contraindicacoes: "Reação anafilática grave a doses anteriores."
      }
    ];

    const DATA_INDICADORES = [
      {
        id: "C1",
        codigo: "C1",
        titulo: "Proporção de Atendimentos por Demanda Programada",
        eixo: "Acesso e Organização",
        objetivo: "Verificar a relação de atendimentos de demanda programada realizados por profissionais da APS e o total de atendimentos realizados.",
        formula: "Numerador: Nº total de atendimentos por demanda programada / Denominador: Nº total de todos os tipos de atendimento.",
        parametro: { otimo: "> 50 e ≤ 70%", bom: "> 30 e ≤ 50%", suficiente: "> 10 e ≤ 30%", regular: "≤ 10 ou > 70%" },
        boasPraticas: [
          "Organização de agenda com equilíbrio entre demanda espontânea e programada.",
          "Manutenção do acompanhamento continuado dos grupos prioritários."
        ],
        cbos: ["2251-42 (EqSF)", "2235-65 (Enf EqSF)", "2235-05 (Enfermeiro)"],
        procedimentos: [],
        cid10: ["Não se aplicam regras específicas"],
        ciap2: ["Não se aplicam regras específicas"]
      },
      {
        id: "C2",
        codigo: "C2",
        titulo: "Cuidado no Desenvolvimento Infantil (Até 2 Anos)",
        eixo: "Saúde da Criança",
        objetivo: "Avaliar o acesso e monitoramento efetivo das crianças até 2 anos em relação aos episódios de cuidados necessários.",
        formula: "Somatório das boas práticas pontuadas para cada criança / Nº total de crianças ≤ 2 anos vinculadas.",
        parametro: { otimo: "> 75 e ≤ 100", bom: "> 50 e ≤ 75", suficiente: "> 25 e ≤ 50", regular: "≤ 25" },
        boasPraticas: [
          "A) 1ª consulta presencial por médico/enfermeiro até o 30º dia de vida (20 pts)",
          "B) Pelo menos 9 consultas presenciais/remotas por médico/enfermeiro até 2 anos (20 pts)",
          "C) Pelo menos 9 registros simultâneos de peso e altura até 2 anos (20 pts)",
          "D) Pelo menos 2 VDs por ACS/TACS (20 pts)",
          "E) Vacinas em dia: Penta, Poliomielite (VIP), Tríplice Viral, Pneumocócica (20 pts)"
        ],
        cbos: ["2235 (Enfermeiros)", "2231/2251 (Médicos)", "5151-05 (ACS)"],
        procedimentos: [
          { cod: "01.01.04.002-4", desc: "Avaliação antropométrica" },
          { cod: "03.01.01.026-9", desc: "Avaliação do crescimento na puericultura" },
          { cod: "03.01.01.027-7", desc: "Avaliação do desenvolvimento da criança na puericultura" }
        ],
        vacinas: ["09 (Hepatite B)", "42 (Penta)", "22 (VIP Polio)", "24 (Tríplice Viral SCR)"],
        cid10: ["Não se aplicam regras específicas"],
        ciap2: ["Não se aplicam regras específicas"]
      },
      {
        id: "C3",
        codigo: "C3",
        titulo: "Cuidado na Gestação e Puerpério",
        eixo: "Saúde da Mulher / Materno-Infantil",
        objetivo: "Avaliar o acesso e monitoramento efetivo durante a gestação e puerpério.",
        formula: "Somatório das boas práticas pontuadas para cada gestante/puérpera / Nº total de gestantes/puérperas.",
        parametro: { otimo: "> 75 e ≤ 100", bom: "> 50 e ≤ 75", suficiente: "> 25 e ≤ 50", regular: "≤ 25" },
        boasPraticas: [
          "A) 1ª consulta até a 12ª semana de gestação (10 pts)",
          "B) Pelo menos 7 consultas pré-natais (9 pts)",
          "C) Pelo menos 7 registros de PA (9 pts)",
          "D) Vacina dTpa a partir da 20ª semana (9 pts)",
          "E) Testes rápidos/exames no 1º e 3º trimestres (18 pts)",
          "F) Consulta e VD no puerpério (18 pts)"
        ],
        cbos: ["2235 (Enfermeiros)", "2231/2251 (Médicos)", "5151-05 (ACS)"],
        procedimentos: [
          { cod: "03.01.01.011-0", desc: "Consulta pré-natal" },
          { cod: "03.01.01.012-9", desc: "Consulta puerperal" },
          { cod: "02.14.01.008-2", desc: "TR para sífilis na gestante" }
        ],
        vacinas: ["57 (Vacina dTpa adulto)"],
        cid10: ["Z34 (Supervisão de gravidez normal)", "Z39 (Exame no pós-parto)"],
        ciap2: ["W78 (Gravidez)", "W84 (Pré-natal)"]
      },
      {
        id: "C4",
        codigo: "C4",
        titulo: "Cuidado da Pessoa com Diabetes",
        eixo: "Condições Crônicas",
        objetivo: "Avaliar o acompanhamento contínuo e monitoramento efetivo das pessoas com Diabetes Mellitus na APS.",
        formula: "Somatório das boas práticas / Nº total de pessoas com diabetes vinculadas.",
        parametro: { otimo: "> 75 e ≤ 100", bom: "> 50 e ≤ 75", suficiente: "> 25 e ≤ 50", regular: "≤ 25" },
        boasPraticas: [
          "A) Consulta presencial/remota nos últimos 6 meses (20 pts)",
          "B) Aferição de PA nos últimos 6 meses (15 pts)",
          "C) Avaliação/solicitação de HbA1c nos últimos 12 meses (15 pts)",
          "D) Exame do pé diabético nos últimos 12 meses (15 pts)"
        ],
        cbos: ["2235 (Enfermeiros)", "2231/2251 (Médicos)"],
        procedimentos: [
          { cod: "03.01.04.009-5", desc: "Exame do pé diabético" },
          { cod: "02.02.01.050-3", desc: "Dosagem de hemoglobina glicosilada (HbA1c)" }
        ],
        cid10: ["E10 (Diabetes tipo 1)", "E11 (Diabetes tipo 2)"],
        ciap2: ["T90 (Diabetes mellitus)"]
      },
      {
        id: "C5",
        codigo: "C5",
        titulo: "Cuidado da Pessoa com Hipertensão Arterial",
        eixo: "Condições Crônicas",
        objetivo: "Avaliar o acesso e acompanhamento contínuo das pessoas com Hipertensão Arterial Sistêmica.",
        formula: "Somatório das boas práticas / Nº total de hipertensos vinculados.",
        parametro: { otimo: "> 75 e ≤ 100", bom: "> 50 e ≤ 75", suficiente: "> 25 e ≤ 50", regular: "≤ 25" },
        boasPraticas: [
          "A) Consulta médica/enfermagem nos últimos 6 meses (25 pts)",
          "B) Aferição de Pressão Arterial nos últimos 6 meses (25 pts)",
          "C) Antropometria nos últimos 12 meses (25 pts)",
          "D) 2 VDs por ACS/TACS nos últimos 12 meses (25 pts)"
        ],
        cbos: ["2235 (Enfermeiros)", "2231/2251 (Médicos)"],
        procedimentos: [
          { cod: "03.01.10.003-9", desc: "Aferição da pressão arterial" },
          { cod: "01.01.04.002-4", desc: "Avaliação antropométrica" }
        ],
        cid10: ["I10 (Hipertensão essencial)"],
        ciap2: ["K86 (Hipertensão sem complicações)"]
      },
      {
        id: "C6",
        codigo: "C6",
        titulo: "Cuidado da Pessoa Idosa (60 anos ou mais)",
        eixo: "Saúde do Idoso",
        objetivo: "Avaliar o acesso e acompanhamento efetivo das pessoas idosas na APS.",
        formula: "Somatório das boas práticas por idoso / Nº total de idosos vinculados.",
        parametro: { otimo: "> 75 e ≤ 100", bom: "> 50 e ≤ 75", suficiente: "> 25 e ≤ 50", regular: "≤ 25" },
        boasPraticas: [
          "A) Consulta nos últimos 12 meses (25 pts)",
          "B) Antropometria nos últimos 12 meses (25 pts)",
          "C) 2 VDs por ACS nos últimos 12 meses (25 pts)",
          "D) Vacina Influenza nos últimos 12 meses (25 pts)"
        ],
        cbos: ["2235 (Enfermeiros)", "2231/2251 (Médicos)"],
        procedimentos: [
          { cod: "01.01.04.002-4", desc: "Avaliação antropométrica" }
        ],
        vacinas: ["33 (Vacina influenza trivalente)"],
        cid10: ["Não se aplicam regras específicas"],
        ciap2: ["Não se aplicam regras específicas"]
      },
      {
        id: "C7",
        codigo: "C7",
        titulo: "Cuidado na Prevenção do Câncer de Colo do Útero e Mama",
        eixo: "Saúde da Mulher / Homens Trans",
        objetivo: "Avaliar o rastreamento efetivo para os cânceres de colo do útero e mama.",
        formula: "Somatório das boas práticas / Nº total de pessoas elegíveis vinculadas.",
        parametro: { otimo: "> 75 e ≤ 100", bom: "> 50 e ≤ 75", suficiente: "> 25 e ≤ 50", regular: "≤ 25" },
        boasPraticas: [
          "A) Papanicolau nos últimos 36 meses (20 pts)",
          "B) Vacina HPV para meninas de 9 a 14 anos (30 pts)",
          "C) Atendimento em saúde sexual e reprodutiva nos últimos 12 meses (30 pts)",
          "D) Mamografia nos últimos 24 meses (20 pts)"
        ],
        cbos: ["2235 (Enfermeiros)", "2231/2251 (Médicos)"],
        procedimentos: [
          { cod: "02.01.02.003-3", desc: "Coleta de citopatológico de colo uterino" },
          { cod: "02.04.03.018-8", desc: "Mamografia bilateral para rastreamento" }
        ],
        vacinas: ["67 (Vacina HPV quadrivalente)"],
        cid10: ["Z12.4 (Rastreamento de CA de colo uterino)"],
        ciap2: ["X11 (Papanicolau/Citologia uterina)"]
      }
    ];

    const DATA_PRESCRICAO = [
      {
        tipo: "Rotina / SAE",
        medicamento: "Dipirona Sódica",
        apresentacao: "Comprimido 500mg, Gotas 500mg/mL, Ampola 500mg/2mL",
        indicacoes: "Alívio da dor leve a moderada e quadros febris.",
        posologia: "Adultos: 500 a 1000 mg/dose até 4x/dia. Crianças: 10 a 25 mg/kg/dose 4x/dia.",
        contraindicacoes: "Menores de 3 meses ou < 5kg, neutropenia, porfiria.",
        gestacaoLactacao: "Evitar no 1º e 3º trimestres da gravidez."
      },
      {
        tipo: "Rotina / SAE",
        medicamento: "Paracetamol",
        apresentacao: "Comprimido 500mg ou 750mg, Gotas 200mg/mL",
        indicacoes: "Analgésico e antipirético de 1ª linha.",
        posologia: "Adultos: 500 a 1000 mg/dose a cada 6-8h (Máx: 4g/dia). Crianças: 10 a 15 mg/kg/dose.",
        contraindicacoes: "Doenças hepáticas graves, alcoolismo.",
        gestacaoLactacao: "Seguro na gravidez e amamentação para uso em períodos curtos."
      },
      {
        tipo: "Rotina / SAE",
        medicamento: "Levonorgestrel (Contracepção de Emergência)",
        apresentacao: "Comprimido 0,75mg (2 comp) ou 1,5mg (dose única)",
        indicacoes: "Prevenção da gravidez após relação sexual desprotegida.",
        posologia: "Tomar 1,5 mg em dose única até 72 horas após a relação.",
        contraindicacoes: "Gravidez confirmada (não possui efeito abortivo).",
        gestacaoLactacao: "Contraindicado na gestação. Amamentação segura."
      },
      {
        tipo: "Rotina / SAE",
        medicamento: "Ácido Fólico",
        apresentacao: "Comprimido 5mg",
        indicacoes: "Prevenção de defeitos no fechamento do tubo neural do feto.",
        posologia: "4 a 5 mg/dia, iniciando 4 semanas antes da concepção até a 12ª semana gestacional.",
        contraindicacoes: "Anemia perniciosa não tratada.",
        gestacaoLactacao: "Seguro e recomendado no início da gestação."
      },
      {
        tipo: "Medidas de Conforto",
        medicamento: "Salbutamol / Fenoterol (Broncodilatadores)",
        apresentacao: "Salbutamol Spray 100mcg/dose; Fenoterol Solução 5mg/mL",
        indicacoes: "Medida de conforto em crises de asma leve/moderada.",
        posologia: "Inalação/Nebulização conforme protocolo. NUNCA usar água bidestilada como veículo (usar SF 0,9%).",
        contraindicacoes: "Hipersensibilidade, taquiarritmias graves.",
        gestacaoLactacao: "Uso sob monitoramento clínico."
      }
    ];


    let currentTab = 'portfolio';
    let currentFilterCategory = 'ALL';
    let searchQuery = '';

    window.addEventListener('DOMContentLoaded', () => {
      renderAllTabs();
      setupSearchEvents();
    });

    function switchTab(tabName) {
      currentTab = tabName;
      currentFilterCategory = 'ALL';
      
      // Update UI Tabs
      document.querySelectorAll('.tab-btn').forEach(btn => {
        btn.classList.remove('bg-teal-700', 'text-white', 'shadow-inner');
      });
      document.getElementById(`tab-${tabName}`).classList.add('bg-teal-700', 'text-white', 'shadow-inner');

      // Update Tab Content Sections
      document.querySelectorAll('.tab-content').forEach(sec => sec.classList.add('hidden'));
      document.getElementById(`section-${tabName}`).classList.remove('hidden');

      // Render Sub-filters and Items
      renderSubFilters();
      applyFiltersAndSearch();
    }


    function renderSubFilters() {
      const filterContainer = document.getElementById('filterCategoryButtons');
      filterContainer.innerHTML = '';

      let categories = ['ALL'];

      if (currentTab === 'portfolio') {
        categories = ['ALL', 'Contexto', 'Evidências Científicas', 'Percepções do Estudante', 'Reflexão Crítica', 'Proposições'];
      } else if (currentTab === 'exames') {
        categories = ['ALL', 'Pré-Natal / Hematologia', 'Infectologia / Sorologias', 'Infectologia / Respiratório', 'Saúde da Mulher / Rastreamento', 'Saúde da Mulher / Planejamento', 'Saúde da Mulher / Ultrassonografia', 'Condições Crônicas / Risco CV', 'Renal / Condições Crônicas', 'Renal / Diabetes', 'Endocrinologia / Diabetes', 'Endocrinologia / Gestação', 'Endocrinologia / Rastreamento', 'Eletrólitos / Cardio-Renal', 'Cardiovascular / Geral', 'Hematologia / Geral', 'Gastroenterologia / Parasitologia', 'Saúde do Homem / Planejamento', 'Urologia / Rotina', 'Geral / Microbiologia'];
      } else if (currentTab === 'vacinacao') {
        categories = ['ALL', 'Criança', 'Adolescente / Jovem', 'Adulto / Idoso', 'Gestante'];
      } else if (currentTab === 'indicadores') {
        categories = ['ALL', 'Acesso e Organização', 'Saúde da Criança', 'Saúde da Mulher / Materno-Infantil', 'Condições Crônicas', 'Saúde do Idoso', 'Saúde da Mulher / Homens Trans'];
      } else if (currentTab === 'prescricao') {
        categories = ['ALL', 'Rotina / SAE', 'Medidas de Conforto'];
      } else if (currentTab === 'codigos') {
        categories = ['ALL', 'PROCEDIMENTO', 'VACINA', 'CID10', 'CIAP2'];
      }

      categories.forEach(cat => {
        const btn = document.createElement('button');
        const isSelected = currentFilterCategory === cat;
        btn.className = `px-2.5 py-1 rounded-full border text-xs font-medium transition ${
          isSelected 
            ? 'bg-teal-700 text-white border-teal-700 shadow-sm' 
            : 'bg-slate-100 text-slate-600 border-slate-200 hover:bg-slate-200'
        }`;
        btn.textContent = cat === 'ALL' ? 'Todos' : cat;
        btn.onclick = () => {
          currentFilterCategory = cat;
          renderSubFilters();
          applyFiltersAndSearch();
        };
        filterContainer.appendChild(btn);
      });
    }


    function renderAllTabs() {
      renderSubFilters();
      renderExamesCards();
      renderVacinacaoCards();
      renderIndicadoresCards();
      renderPrescricaoCards();
      renderCodesTable();
      applyFiltersAndSearch();
    }

    // 1. EXAMES CARDS
    function renderExamesCards() {
      const container = document.getElementById('examesCardsContainer');
      container.innerHTML = '';

      DATA_EXAMES_PBH.forEach(item => {
        const card = document.createElement('div');
        card.className = "exame-card bg-white rounded-xl border border-slate-200 shadow-sm hover:shadow-md transition flex flex-col overflow-hidden";
        card.dataset.categoria = item.categoria;
        card.dataset.search = `${item.nome} ${item.categoria} ${item.indicacoes} ${item.finalidade} ${item.orientacoes}`.toLowerCase();

        card.innerHTML = `
          <div class="p-3.5 bg-slate-800 text-white flex items-center justify-between">
            <span class="text-[11px] font-semibold px-2 py-0.5 rounded bg-emerald-500/20 text-emerald-300 border border-emerald-500/30">
              ${item.categoria}
            </span>
            <button onclick="openExameModal('${item.id}')" class="text-xs bg-white/10 hover:bg-white/20 text-white px-2 py-1 rounded transition flex items-center gap-1">
              <i class="fa-solid fa-expand"></i> Detalhes
            </button>
          </div>
          <div class="p-4 flex-1 flex flex-col justify-between space-y-3">
            <div>
              <h3 class="font-bold text-slate-800 text-base leading-snug text-teal-800 mb-2">${item.nome}</h3>
              <div class="space-y-2 text-xs">
                <div>
                  <span class="font-bold text-slate-700 block"><i class="fa-solid fa-bullseye text-teal-600 me-1"></i> Finalidade Clínica:</span>
                  <p class="text-slate-600 mt-0.5 leading-relaxed">${item.finalidade}</p>
                </div>
                <div>
                  <span class="font-bold text-slate-700 block"><i class="fa-solid fa-user-check text-indigo-600 me-1"></i> Indicações:</span>
                  <p class="text-slate-600 mt-0.5">${item.indicacoes}</p>
                </div>
              </div>
            </div>
            <div class="bg-slate-50 border border-slate-200 rounded-lg p-2.5 text-[11px] text-slate-600">
              <span class="font-bold text-slate-700"><i class="fa-solid fa-circle-info text-amber-500 me-1"></i> Orientação / Conduta:</span> ${item.orientacoes}
            </div>
          </div>
        `;
        container.appendChild(card);
      });
    }

    // 2. VACINAÇÃO 2026 CARDS
    function renderVacinacaoCards() {
      const container = document.getElementById('vacinacaoCardsContainer');
      container.innerHTML = '';

      DATA_VACINAS_2026.forEach(item => {
        const card = document.createElement('div');
        card.className = "vacina-card bg-white rounded-xl border border-slate-200 shadow-sm hover:shadow-md transition flex flex-col overflow-hidden";
        
        let cicloClass = "bg-amber-100 text-amber-800 border-amber-300";
        if(item.ciclo === 'Criança') cicloClass = "bg-blue-100 text-blue-800 border-blue-300";
        if(item.ciclo === 'Adolescente / Jovem') cicloClass = "bg-indigo-100 text-indigo-800 border-indigo-300";
        if(item.ciclo === 'Gestante') cicloClass = "bg-rose-100 text-rose-800 border-rose-300";
        if(item.ciclo.includes('Idoso')) cicloClass = "bg-emerald-100 text-emerald-800 border-emerald-300";

        card.dataset.ciclo = item.ciclo.includes('Idoso') ? 'Adulto / Idoso' : item.ciclo;
        card.dataset.search = `${item.vacina} ${item.ciclo} ${item.protecao} ${item.esquema} ${item.particularidades} ${item.contraindicacoes}`.toLowerCase();

        card.innerHTML = `
          <div class="p-3.5 bg-gradient-to-r from-teal-800 to-teal-700 text-white flex items-center justify-between">
            <span class="text-xs font-bold px-2 py-0.5 rounded border ${cicloClass}">
              ${item.ciclo}
            </span>
            <button onclick="openVacinaModal('${item.id}')" class="text-xs bg-white/10 hover:bg-white/20 text-white px-2.5 py-1 rounded-lg transition border border-white/20 flex items-center gap-1">
              <i class="fa-solid fa-expand"></i> Ficha Técnica
            </button>
          </div>
          <div class="p-4 flex-1 flex flex-col justify-between space-y-3">
            <div>
              <h3 class="font-bold text-slate-800 text-base text-teal-900 mb-1">${item.vacina}</h3>
              <p class="text-xs text-slate-600 mb-2"><strong class="text-slate-700">Proteção:</strong> ${item.protecao}</p>
              
              <div class="bg-teal-50/60 border border-teal-100 p-2.5 rounded-lg text-xs space-y-1">
                <div><strong class="text-teal-900"><i class="fa-solid fa-calendar-check me-1"></i> Esquema:</strong> ${item.esquema}</div>
                <div><strong class="text-teal-900"><i class="fa-solid fa-arrows-rotate me-1"></i> Reforço / Intervalo:</strong> ${item.reforco || item.intervalo}</div>
              </div>
            </div>

            <div class="text-[11px] space-y-1.5 border-t border-slate-100 pt-2 text-slate-600">
              <p><strong class="text-indigo-800"><i class="fa-solid fa-syringe me-1"></i> Via/Volume:</strong> ${item.viaVol}</p>
              <p class="line-clamp-2"><strong class="text-rose-700"><i class="fa-solid fa-triangle-exclamation me-1"></i> Contraindicações:</strong> ${item.contraindicacoes}</p>
            </div>
          </div>
        `;
        container.appendChild(card);
      });
    }


    // 3. INDICADORES CARDS
    function renderIndicadoresCards() {
      const container = document.getElementById('indicadoresCardsContainer');
      container.innerHTML = '';

      DATA_INDICADORES.forEach(item => {
        const card = document.createElement('div');
        card.className = "indicador-card bg-white rounded-xl border border-slate-200 shadow-sm hover:shadow-md transition flex flex-col overflow-hidden";
        card.dataset.eixo = item.eixo;
        card.dataset.search = `${item.codigo} ${item.titulo} ${item.objetivo} ${item.eixo} ${item.cbos.join(' ')}`.toLowerCase();

        card.innerHTML = `
          <div class="p-4 bg-gradient-to-r from-teal-800 to-teal-700 text-white flex items-center justify-between">
            <div class="flex items-center space-x-2">
              <span class="bg-amber-400 text-slate-900 font-extrabold text-xs px-2.5 py-1 rounded-md shadow-sm">${item.codigo}</span>
              <span class="text-xs font-semibold text-teal-100 uppercase tracking-wider">${item.eixo}</span>
            </div>
            <button onclick="openIndicadorModal('${item.id}')" class="text-xs bg-white/10 hover:bg-white/20 text-white px-2.5 py-1 rounded-lg transition border border-white/20 flex items-center gap-1">
              <i class="fa-solid fa-expand"></i> Detalhes
            </button>
          </div>

          <div class="p-4 flex-1 flex flex-col justify-between space-y-3">
            <div>
              <h3 class="font-bold text-slate-800 text-sm leading-snug mb-1">${item.titulo}</h3>
              <p class="text-xs text-slate-600 line-clamp-2">${item.objetivo}</p>
            </div>

            <div class="bg-amber-50/70 border border-amber-200/80 rounded-lg p-2.5">
              <div class="text-[11px] font-bold text-amber-900 mb-1 flex items-center gap-1">
                <i class="fa-solid fa-bullseye text-amber-600"></i> Metas / Parâmetros:
              </div>
              <div class="grid grid-cols-2 gap-1 text-[11px] text-slate-700">
                <div><span class="font-bold text-emerald-700">Ótimo:</span> ${item.parametro.otimo}</div>
                <div><span class="font-bold text-blue-700">Bom:</span> ${item.parametro.bom}</div>
              </div>
            </div>

            <div class="border-t border-slate-100 pt-2 flex items-center justify-between text-xs">
              <span class="text-slate-500 font-medium"><i class="fa-solid fa-stethoscope text-teal-600 me-1"></i> CBOs Habilitados:</span>
              <span class="text-slate-700 font-bold bg-slate-100 px-2 py-0.5 rounded text-[11px]">${item.cbos.length} CBOs</span>
            </div>
          </div>
        `;
        container.appendChild(card);
      });
    }

    // 4. PRESCRIÇÃO CARDS
    function renderPrescricaoCards() {
      const container = document.getElementById('prescricaoCardsContainer');
      container.innerHTML = '';

      DATA_PRESCRICAO.forEach(item => {
        const card = document.createElement('div');
        card.className = "prescricao-card bg-white rounded-xl border border-slate-200 shadow-sm hover:shadow-md transition flex flex-col overflow-hidden";
        card.dataset.tipo = item.tipo;
        card.dataset.search = `${item.medicamento} ${item.apresentacao} ${item.indicacoes} ${item.posologia}`.toLowerCase();

        const badgeBg = item.tipo.includes('Confor') ? 'bg-amber-500/20 text-amber-300 border-amber-500/30' : 'bg-cyan-500/20 text-cyan-300 border-cyan-500/30';

        card.innerHTML = `
          <div class="p-3.5 bg-slate-900 text-white flex items-center justify-between">
            <span class="text-xs font-semibold px-2 py-0.5 rounded border ${badgeBg}">
              ${item.tipo}
            </span>
            <i class="fa-solid fa-pills text-cyan-400"></i>
          </div>
          <div class="p-4 flex-1 flex flex-col justify-between space-y-3">
            <div>
              <h3 class="font-bold text-slate-800 text-base text-cyan-900">${item.medicamento}</h3>
              <p class="text-xs text-slate-500 font-medium mb-3">${item.apresentacao}</p>
              
              <div class="space-y-2 text-xs">
                <div>
                  <span class="font-bold text-slate-700 block"><i class="fa-solid fa-stethoscope text-teal-600 me-1"></i> Indicação:</span>
                  <p class="text-slate-600 mt-0.5">${item.indicacoes}</p>
                </div>
                <div class="bg-cyan-50 border border-cyan-200/60 p-2.5 rounded-lg">
                  <span class="font-bold text-cyan-900 block"><i class="fa-solid fa-clock text-cyan-700 me-1"></i> Posologia Preconizada:</span>
                  <p class="text-cyan-800 font-medium mt-0.5 text-[11px]">${item.posologia}</p>
                </div>
              </div>
            </div>

            <div class="text-[11px] space-y-1 border-t border-slate-100 pt-2 text-slate-600">
              <p><strong class="text-rose-700"><i class="fa-solid fa-triangle-exclamation me-1"></i> Contraindicações:</strong> ${item.contraindicacoes}</p>
              <p><strong class="text-indigo-700"><i class="fa-solid fa-baby-carriage me-1"></i> Gravidez / Lactação:</strong> ${item.gestacaoLactacao}</p>
            </div>
          </div>
        `;
        container.appendChild(card);
      });
    }

    // 5. CODES TABLE
    function renderCodesTable() {
      const tbody = document.getElementById('codesTableBody');
      tbody.innerHTML = '';

      let rows = [];

      DATA_INDICADORES.forEach(ind => {
        ind.procedimentos.forEach(p => {
          rows.push({
            indicador: ind.codigo,
            tipo: 'PROCEDIMENTO',
            codigo: p.cod,
            descricao: p.desc
          });
        });
        if (ind.vacinas) {
          ind.vacinas.forEach(v => {
            rows.push({
              indicador: ind.codigo,
              tipo: 'VACINA',
              codigo: v.split(' ')[0],
              descricao: v
            });
          });
        }
        ind.cid10.forEach(c => {
          rows.push({
            indicador: ind.codigo,
            tipo: 'CID10',
            codigo: c.split(' ')[0],
            descricao: c
          });
        });
        ind.ciap2.forEach(c => {
          rows.push({
            indicador: ind.codigo,
            tipo: 'CIAP2',
            codigo: c.split(' ')[0],
            descricao: c
          });
        });
      });

      DATA_VACINAS_2026.forEach(v => {
        rows.push({
          indicador: `PNI (${v.ciclo})`,
          tipo: 'VACINA',
          codigo: v.id.replace('VAC_', ''),
          descricao: `${v.vacina} - ${v.protecao}`
        });
      });

      rows.forEach(r => {
        const tr = document.createElement('tr');
        tr.className = "code-row hover:bg-slate-50 transition";
        tr.dataset.tipo = r.tipo;
        tr.dataset.search = `${r.indicador} ${r.tipo} ${r.codigo} ${r.descricao}`.toLowerCase();

        let badgeStyle = "bg-slate-100 text-slate-700";
        if (r.tipo === 'PROCEDIMENTO') badgeStyle = "bg-emerald-100 text-emerald-800 font-bold";
        if (r.tipo === 'CID10') badgeStyle = "bg-indigo-100 text-indigo-800 font-bold";
        if (r.tipo === 'CIAP2') badgeStyle = "bg-amber-100 text-amber-800 font-bold";
        if (r.tipo === 'VACINA') badgeStyle = "bg-cyan-100 text-cyan-800 font-bold";

        tr.innerHTML = `
          <td class="p-3 font-extrabold text-teal-800">${r.indicador}</td>
          <td class="p-3"><span class="px-2 py-0.5 rounded text-[10px] ${badgeStyle}">${r.tipo}</span></td>
          <td class="p-3 font-mono font-bold text-slate-900">${r.codigo}</td>
          <td class="p-3 text-slate-600">${r.descricao}</td>
          <td class="p-3 text-right">
            <button onclick="copyToClipboard('${r.codigo}')" class="text-xs bg-slate-100 hover:bg-teal-700 hover:text-white text-slate-700 px-2.5 py-1 rounded-lg transition border border-slate-200 inline-flex items-center gap-1">
              <i class="fa-regular fa-copy"></i> Copiar
            </button>
          </td>
        `;
        tbody.appendChild(tr);
      });
    }


    function setupSearchEvents() {
      const searchInput = document.getElementById('searchInput');
      const clearSearch = document.getElementById('clearSearch');

      searchInput.addEventListener('input', (e) => {
        searchQuery = e.target.value.trim().toLowerCase();
        if (searchQuery.length > 0) {
          clearSearch.classList.remove('hidden');
        } else {
          clearSearch.classList.add('hidden');
        }
        applyFiltersAndSearch();
      });

      clearSearch.addEventListener('click', () => {
        searchInput.value = '';
        searchQuery = '';
        clearSearch.classList.add('hidden');
        applyFiltersAndSearch();
      });
    }

    function filterCodesTable() {
      const selectVal = document.getElementById('codeTypeFilter').value;
      document.querySelectorAll('.code-row').forEach(row => {
        const matchesType = selectVal === 'ALL' || row.dataset.tipo === selectVal;
        const matchesSearch = searchQuery === '' || row.dataset.search.includes(searchQuery);
        if (matchesType && matchesSearch) {
          row.classList.remove('hidden');
        } else {
          row.classList.add('hidden');
        }
      });
    }

    function applyFiltersAndSearch() {
      let visibleCount = 0;
      let totalCount = 0;

      if (currentTab === 'portfolio') {
        const cards = document.querySelectorAll('.portfolio-card');
        totalCount = cards.length;
        cards.forEach(card => {
          const matchesCategory = currentFilterCategory === 'ALL' || card.dataset.section === currentFilterCategory;
          const matchesSearch = searchQuery === '' || card.dataset.search.includes(searchQuery);
          if (matchesCategory && matchesSearch) {
            card.classList.remove('hidden');
            visibleCount++;
          } else {
            card.classList.add('hidden');
          }
        });
      } else if (currentTab === 'exames') {
        const cards = document.querySelectorAll('.exame-card');
        totalCount = cards.length;
        cards.forEach(card => {
          const matchesCategory = currentFilterCategory === 'ALL' || card.dataset.categoria === currentFilterCategory;
          const matchesSearch = searchQuery === '' || card.dataset.search.includes(searchQuery);
          if (matchesCategory && matchesSearch) {
            card.classList.remove('hidden');
            visibleCount++;
          } else {
            card.classList.add('hidden');
          }
        });
      } else if (currentTab === 'vacinacao') {
        const cards = document.querySelectorAll('.vacina-card');
        totalCount = cards.length;
        cards.forEach(card => {
          const matchesCategory = currentFilterCategory === 'ALL' || card.dataset.ciclo === currentFilterCategory;
          const matchesSearch = searchQuery === '' || card.dataset.search.includes(searchQuery);
          if (matchesCategory && matchesSearch) {
            card.classList.remove('hidden');
            visibleCount++;
          } else {
            card.classList.add('hidden');
          }
        });
      } else if (currentTab === 'indicadores') {
        const cards = document.querySelectorAll('.indicador-card');
        totalCount = cards.length;
        cards.forEach(card => {
          const matchesCategory = currentFilterCategory === 'ALL' || card.dataset.eixo === currentFilterCategory;
          const matchesSearch = searchQuery === '' || card.dataset.search.includes(searchQuery);
          if (matchesCategory && matchesSearch) {
            card.classList.remove('hidden');
            visibleCount++;
          } else {
            card.classList.add('hidden');
          }
        });
      } else if (currentTab === 'prescricao') {
        const cards = document.querySelectorAll('.prescricao-card');
        totalCount = cards.length;
        cards.forEach(card => {
          const matchesCategory = currentFilterCategory === 'ALL' || card.dataset.tipo === currentFilterCategory;
          const matchesSearch = searchQuery === '' || card.dataset.search.includes(searchQuery);
          if (matchesCategory && matchesSearch) {
            card.classList.remove('hidden');
            visibleCount++;
          } else {
            card.classList.add('hidden');
          }
        });
      } else if (currentTab === 'codigos') {
        const rows = document.querySelectorAll('.code-row');
        totalCount = rows.length;
        const selectVal = document.getElementById('codeTypeFilter');
        if (currentFilterCategory !== 'ALL') {
          selectVal.value = currentFilterCategory;
        } else {
          selectVal.value = 'ALL';
        }
        
        rows.forEach(row => {
          const matchesType = selectVal.value === 'ALL' || row.dataset.tipo === selectVal.value;
          const matchesSearch = searchQuery === '' || row.dataset.search.includes(searchQuery);
          if (matchesType && matchesSearch) {
            row.classList.remove('hidden');
            visibleCount++;
          } else {
            row.classList.add('hidden');
          }
        });
      }

      // Update Results Count Label
      document.getElementById('resultsCount').textContent = `Exibindo ${visibleCount} de ${totalCount} itens`;

      // Show/Hide Empty State
      const emptyState = document.getElementById('emptyState');
      if (visibleCount === 0) {
        emptyState.classList.remove('hidden');
      } else {
        emptyState.classList.add('hidden');
      }
    }


    function openExameModal(id) {
      const item = DATA_EXAMES_PBH.find(x => x.id === id);
      if (!item) return;

      document.getElementById('modalTitle').innerHTML = `
        <span class="bg-emerald-400 text-slate-900 text-xs px-2 py-0.5 rounded font-black"><i class="fa-solid fa-vial"></i> PBH</span>
        <span>${item.nome}</span>
      `;

      document.getElementById('modalBody').innerHTML = `
        <div>
          <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1">Categoria Protocolar</h4>
          <span class="inline-block bg-teal-50 text-teal-800 font-bold text-xs px-2.5 py-1 rounded border border-teal-200">${item.categoria}</span>
        </div>

        <div>
          <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1">Finalidade Clínica</h4>
          <p class="text-slate-700 bg-emerald-50/60 p-3 rounded-lg border border-emerald-100 text-xs leading-relaxed">${item.finalidade}</p>
        </div>

        <div>
          <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1">Indicações Principais</h4>
          <p class="text-xs text-slate-700 bg-slate-100 p-2.5 rounded-lg border border-slate-200">${item.indicacoes}</p>
        </div>

        <div>
          <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1"><i class="fa-solid fa-circle-info text-amber-500 me-1"></i> Orientações Práticas e Conduta</h4>
          <p class="text-xs text-slate-700 bg-amber-50/80 p-3 rounded-lg border border-amber-200">${item.orientacoes}</p>
        </div>
      `;

      showModal();
    }

    function openVacinaModal(id) {
      const item = DATA_VACINAS_2026.find(x => x.id === id);
      if (!item) return;

      document.getElementById('modalTitle').innerHTML = `
        <span class="bg-amber-400 text-slate-900 text-xs px-2 py-0.5 rounded font-black"><i class="fa-solid fa-syringe"></i> ${item.ciclo}</span>
        <span>${item.vacina}</span>
      `;

      document.getElementById('modalBody').innerHTML = `
        <div>
          <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1">Proteção Contra / Indicação</h4>
          <p class="text-slate-700 bg-teal-50/50 p-3 rounded-lg border border-teal-100">${item.protecao}</p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-3">
          <div>
            <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1">Esquema Básico</h4>
            <p class="text-xs text-slate-700 bg-slate-100 p-2.5 rounded-lg border border-slate-200">${item.esquema}</p>
          </div>
          <div>
            <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1">Reforços / Intervalos</h4>
            <p class="text-xs text-slate-700 bg-slate-100 p-2.5 rounded-lg border border-slate-200">${item.reforco || item.intervalo}</p>
          </div>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-3">
          <div>
            <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1">Via & Volume de Adm.</h4>
            <p class="text-xs text-indigo-900 bg-indigo-50 p-2.5 rounded-lg border border-indigo-100 font-medium">${item.viaVol}</p>
          </div>
          <div>
            <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1">Composição</h4>
            <p class="text-xs text-slate-600 bg-slate-50 p-2.5 rounded-lg border border-slate-200">${item.composicao}</p>
          </div>
        </div>

        <div>
          <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1"><i class="fa-solid fa-circle-info text-amber-500 me-1"></i> Particularidades Técnicas</h4>
          <p class="text-xs text-slate-700 bg-amber-50/80 p-3 rounded-lg border border-amber-200">${item.particularidades}</p>
        </div>

        <div>
          <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-rose-800 mb-1"><i class="fa-solid fa-triangle-exclamation text-rose-600 me-1"></i> Contraindicações e Alertas</h4>
          <p class="text-xs text-rose-900 bg-rose-50 p-3 rounded-lg border border-rose-200">${item.contraindicacoes}</p>
        </div>
      `;

      showModal();
    }

    function openIndicadorModal(id) {
      const item = DATA_INDICADORES.find(x => x.id === id);
      if (!item) return;

      document.getElementById('modalTitle').innerHTML = `
        <span class="bg-amber-400 text-slate-900 text-xs px-2 py-0.5 rounded font-black">${item.codigo}</span>
        <span>${item.titulo}</span>
      `;

      let procsHtml = item.procedimentos.length > 0 
        ? item.procedimentos.map(p => `<li class="flex items-center justify-between bg-slate-50 p-2 rounded border border-slate-200"><span class="font-mono font-bold text-teal-800">${p.cod}</span><span class="text-slate-600 text-xs">${p.desc}</span></li>`).join('') 
        : '<p class="text-xs text-slate-500 italic">Não há procedimentos específicos obrigatórios definidos nesta régua.</p>';

      let boasPraticasHtml = item.boasPraticas.map(bp => `<li class="flex items-start gap-2"><i class="fa-solid fa-circle-check text-emerald-600 mt-1 text-xs"></i><span>${bp}</span></li>`).join('');

      document.getElementById('modalBody').innerHTML = `
        <div>
          <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1">Objetivo do Indicador</h4>
          <p class="text-slate-700 bg-teal-50/50 p-3 rounded-lg border border-teal-100">${item.objetivo}</p>
        </div>

        <div>
          <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1">Boas Práticas e Pontuação</h4>
          <ul class="space-y-1.5 text-xs text-slate-700">
            ${boasPraticasHtml}
          </ul>
        </div>

        <div>
          <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1">Fórmula de Cálculo</h4>
          <p class="text-xs text-slate-600 bg-slate-100 p-2.5 rounded-lg border border-slate-200 font-mono">${item.formula}</p>
        </div>

        <div class="grid grid-cols-2 gap-3">
          <div>
            <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1">CBOs Elegíveis</h4>
            <div class="flex flex-wrap gap-1">
              ${item.cbos.map(c => `<span class="bg-slate-100 text-slate-700 text-[11px] px-2 py-0.5 rounded border border-slate-200">${c}</span>`).join('')}
            </div>
          </div>
          <div>
            <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1">Parâmetro de Avaliação</h4>
            <div class="text-xs space-y-1 bg-amber-50 p-2.5 rounded-lg border border-amber-200">
              <div><strong class="text-emerald-700">Ótimo:</strong> ${item.parametro.otimo}</div>
              <div><strong class="text-blue-700">Bom:</strong> ${item.parametro.bom}</div>
              <div><strong class="text-amber-700">Suficiente:</strong> ${item.parametro.suficiente}</div>
              <div><strong class="text-rose-700">Regular:</strong> ${item.parametro.regular}</div>
            </div>
          </div>
        </div>

        <div>
          <h4 class="font-bold text-slate-800 text-xs uppercase tracking-wider text-teal-800 mb-1">Principais Procedimentos (SIGTAP)</h4>
          <ul class="space-y-1">
            ${procsHtml}
          </ul>
        </div>
      `;

      showModal();
    }

    function showModal() {
      const modal = document.getElementById('modalBackdrop');
      const container = document.getElementById('modalContainer');
      modal.classList.remove('hidden');
      setTimeout(() => {
        modal.classList.remove('opacity-0');
        container.classList.remove('scale-95');
      }, 10);
    }

    function closeModal() {
      const modal = document.getElementById('modalBackdrop');
      const container = document.getElementById('modalContainer');
      modal.classList.add('opacity-0');
      container.classList.add('scale-95');
      setTimeout(() => {
        modal.classList.add('hidden');
      }, 200);
    }

    function copyToClipboard(text) {
      if (navigator.clipboard && window.isSecureContext) {
        navigator.clipboard.writeText(text);
      } else {
        const input = document.createElement('input');
        input.value = text;
        document.body.appendChild(input);
        input.select();
        document.execCommand('copy');
        document.body.removeChild(input);
      }
      showToast(`Copiado para a área de transferência!`);
    }

    function showToast(msg) {
      const toast = document.getElementById('toast');
      document.getElementById('toastMsg').textContent = msg;
      toast.classList.remove('translate-y-16', 'opacity-0');
      setTimeout(() => {
        toast.classList.add('translate-y-16', 'opacity-0');
      }, 3000);
    }
  </script>
</body>
</html>r_pidos_de_consulta_enfermagem_aps_pbh.html…]()
# CauanSantos009.github.io
