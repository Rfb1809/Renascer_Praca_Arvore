<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Controle de Frequência e Unção - Igreja</title>
  <!-- Tailwind CSS via CDN -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Chart.js via CDN -->
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
  <!-- Ícones Lucide -->
  <script src="https://unpkg.com/lucide@latest"></script>
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap');
    body {
      font-family: 'Inter', sans-serif;
      background-color: #f8fafc;
    }
    .tab-active {
      border-bottom: 2px solid #2563eb;
      color: #2563eb;
      font-weight: 600;
    }
  </style>
</head>
<body class="text-slate-800 antialiased">

  <!-- Cabeçalho -->
  <header class="bg-slate-900 text-white shadow-md">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex flex-col sm:flex-row justify-between items-center gap-4">
      <div class="flex items-center gap-3">
        <div class="bg-blue-600 p-2 rounded-lg">
          <i data-lucide="church" class="w-6 h-6 text-white"></i>
        </div>
        <div>
          <h1 class="text-xl font-bold tracking-tight">Controle de Frequência por Culto</h1>
          <p class="text-xs text-slate-400">Gestão de Membros, Unção e Ministérios</p>
        </div>
      </div>

      <!-- Botões de Backup / Exportação -->
      <div class="flex flex-wrap items-center gap-2">
        <button onclick="exportarCSV()" class="flex items-center gap-1.5 bg-emerald-600 hover:bg-emerald-700 text-white text-xs font-medium px-3 py-2 rounded-lg transition">
          <i data-lucide="file-spreadsheet" class="w-4 h-4"></i>
          Exportar Excel (CSV)
        </button>
        <button onclick="exportarJSON()" class="flex items-center gap-1.5 bg-slate-700 hover:bg-slate-600 text-white text-xs font-medium px-3 py-2 rounded-lg transition">
          <i data-lucide="download" class="w-4 h-4"></i>
          Backup JSON
        </button>
        <label class="flex items-center gap-1.5 bg-slate-700 hover:bg-slate-600 text-white text-xs font-medium px-3 py-2 rounded-lg transition cursor-pointer">
          <i data-lucide="upload" class="w-4 h-4"></i>
          Restaurar
          <input type="file" id="importFile" accept=".json" class="hidden" onchange="importarJSON(event)" />
        </label>
      </div>
    </div>
  </header>

  <!-- Navegação Principal -->
  <div class="bg-white border-b border-slate-200 sticky top-0 z-10">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 flex gap-6">
      <button id="btn-tab-registro" onclick="mudarAba('registro')" class="py-3.5 text-sm flex items-center gap-2 tab-active transition">
        <i data-lucide="user-plus" class="w-4 h-4"></i>
        Lançamento & Lista de Presença
      </button>
      <button id="btn-tab-graficos" onclick="mudarAba('graficos')" class="py-3.5 text-sm flex items-center gap-2 text-slate-500 hover:text-slate-800 transition">
        <i data-lucide="bar-chart-3" class="w-4 h-4"></i>
        Gráficos & Relatórios
      </button>
    </div>
  </div>

  <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-6">

    <!-- ABA 1: REGISTRO E LISTAGEM -->
    <section id="aba-registro" class="space-y-6">

      <!-- Cards de Resumo por Unção -->
      <div id="cards-uncao" class="grid grid-cols-2 sm:grid-cols-4 lg:grid-cols-8 gap-3">
        <!-- Preenchido dinamicamente via JS -->
      </div>

      <!-- Formulário de Lançamento -->
      <div class="bg-white rounded-xl shadow-sm border border-slate-200 p-5">
        <div class="flex items-center justify-between mb-4">
          <h2 class="text-base font-semibold text-slate-800 flex items-center gap-2">
            <i data-lucide="clipboard-check" class="w-5 h-5 text-blue-600"></i>
            Registrar Presença no Culto
          </h2>
          <span class="text-xs text-slate-500 bg-slate-100 px-2.5 py-1 rounded-full">
            Data e Culto ficam fixos para facilitar o lançamento em lote
          </span>
        </div>

        <form id="form-presenca" onsubmit="adicionarRegistro(event)" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-12 gap-4">
          <!-- Data do Culto -->
          <div class="lg:col-span-2">
            <label class="block text-xs font-medium text-slate-600 mb-1">Data do Culto *</label>
            <input type="date" id="input-data" required class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm focus:outline-none focus:ring-2 focus:ring-blue-500" />
          </div>

          <!-- Tipo de Culto -->
          <div class="lg:col-span-2">
            <label class="block text-xs font-medium text-slate-600 mb-1">Culto / Reunião *</label>
            <select id="input-culto" required class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm bg-white focus:outline-none focus:ring-2 focus:ring-blue-500">
              <option value="Culto de Domingo (Noite)">Domingo (Noite)</option>
              <option value="Culto de Domingo (Manhã)">Domingo (Manhã)</option>
              <option value="Culto de Ensino">Culto de Ensino</option>
              <option value="Culto de Oração">Culto de Oração</option>
              <option value="Culto de Jovens">Culto de Jovens</option>
              <option value="Santa Ceia">Santa Ceia</option>
              <option value="Evento Especial">Evento Especial</option>
            </select>
          </div>

          <!-- Nome da Pessoa -->
          <div class="lg:col-span-3">
            <label class="block text-xs font-medium text-slate-600 mb-1">Nome Completo *</label>
            <input type="text" id="input-nome" list="lista-nomes-salvos" placeholder="Ex: João da Silva" required autocomplete="off"
              onchange="autocompletarDadosPessoa(this.value)"
              class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm focus:outline-none focus:ring-2 focus:ring-blue-500" />
            <datalist id="lista-nomes-salvos"></datalist>
          </div>

          <!-- Unção -->
          <div class="lg:col-span-2">
            <label class="block text-xs font-medium text-slate-600 mb-1">Unção / Cargo *</label>
            <select id="input-uncao" required class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm bg-white focus:outline-none focus:ring-2 focus:ring-blue-500">
              <option value="Membro">Membro</option>
              <option value="Bispo">Bispo</option>
              <option value="Pastor">Pastor</option>
              <option value="Presbítero">Presbítero</option>
              <option value="Diácono">Diácono</option>
              <option value="Aspirante">Aspirante</option>
              <option value="Oficial">Oficial</option>
              <option value="Visitante">Visitante</option>
            </select>
          </div>

          <!-- Ministério -->
          <div class="lg:col-span-2">
            <label class="block text-xs font-medium text-slate-600 mb-1">Ministério *</label>
            <input type="text" id="input-ministerio" list="lista-ministerios" placeholder="Ex: Louvor" required
              class="w-full rounded-lg border border-slate-300 px-3 py-2 text-sm focus:outline-none focus:ring-2 focus:ring-blue-500" />
            <datalist id="lista-ministerios">
              <option value="Geral / Sem Ministério">
              <option value="Louvor e Adoração">
              <option value="Infantil (Kids)">
              <option value="Jovens">
              <option value="Casais">
              <option value="Intercessão">
              <option value="Recepção / Diaconato">
              <option value="Mídia e Som">
              <option value="Evangelismo e Missões">
              <option value="Ensino / EBD">
            </datalist>
          </div>

          <!-- Botão Adicionar -->
          <div class="lg:col-span-1 flex items-end">
            <button type="submit" class="w-full bg-blue-600 hover:bg-blue-700 text-white font-medium py-2 px-3 rounded-lg text-sm flex items-center justify-center gap-1 transition shadow-sm">
              <i data-lucide="plus" class="w-4 h-4"></i>
              Salvar
            </button>
          </div>
        </form>
      </div>

      <!-- Filtros e Tabela de Registros -->
      <div class="bg-white rounded-xl shadow-sm border border-slate-200 overflow-hidden">
        <!-- Barra de Filtros -->
        <div class="p-4 bg-slate-50 border-b border-slate-200 grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-5 gap-3 items-end">
          <div>
            <label class="block text-xs font-medium text-slate-500 mb-1">Filtrar por Data</label>
            <input type="date" id="filtro-data" onchange="renderizarTudo()" class="w-full rounded-lg border border-slate-300 px-2.5 py-1.5 text-sm bg-white" />
          </div>
          <div>
            <label class="block text-xs font-medium text-slate-500 mb-1">Filtrar por Unção</label>
            <select id="filtro-uncao" onchange="renderizarTudo()" class="w-full rounded-lg border border-slate-300 px-2.5 py-1.5 text-sm bg-white">
              <option value="">Todas as Unções</option>
              <option value="Bispo">Bispo</option>
              <option value="Pastor">Pastor</option>
              <option value="Presbítero">Presbítero</option>
              <option value="Diácono">Diácono</option>
              <option value="Aspirante">Aspirante</option>
              <option value="Oficial">Oficial</option>
              <option value="Membro">Membro</option>
              <option value="Visitante">Visitante</option>
            </select>
          </div>
          <div>
            <label class="block text-xs font-medium text-slate-500 mb-1">Filtrar por Ministério</label>
            <input type="text" id="filtro-ministerio" oninput="renderizarTudo()" placeholder="Digite o ministério..." class="w-full rounded-lg border border-slate-300 px-2.5 py-1.5 text-sm bg-white" />
          </div>
          <div>
            <label class="block text-xs font-medium text-slate-500 mb-1">Buscar Pessoa</label>
            <input type="text" id="filtro-nome" oninput="renderizarTudo()" placeholder="Nome..." class="w-full rounded-lg border border-slate-300 px-2.5 py-1.5 text-sm bg-white" />
          </div>
          <div class="flex gap-2">
            <button onclick="limparFiltros()" class="w-full bg-white hover:bg-slate-100 text-slate-700 border border-slate-300 font-medium py-1.5 px-3 rounded-lg text-sm transition">
              Limpar Filtros
            </button>
          </div>
        </div>

        <!-- Cabeçalho da Tabela -->
        <div class="px-5 py-3 border-b border-slate-200 flex justify-between items-center">
          <span class="text-sm font-semibold text-slate-700">
            Registros Encontrados: <span id="contador-filtrado" class="text-blue-600">0</span>
          </span>
          <button onclick="limparTodosDados()" class="text-xs text-red-500 hover:text-red-700 hover:underline">
            Apagar todos os dados
          </button>
        </div>

        <!-- Tabela -->
        <div class="overflow-x-auto">
          <table class="w-full text-left border-collapse">
            <thead>
              <tr class="bg-slate-50 text-slate-500 text-xs uppercase tracking-wider border-b border-slate-200">
                <th class="py-3 px-4 font-semibold">Data</th>
                <th class="py-3 px-4 font-semibold">Culto</th>
                <th class="py-3 px-4 font-semibold">Nome</th>
                <th class="py-3 px-4 font-semibold">Unção</th>
                <th class="py-3 px-4 font-semibold">Ministério</th>
                <th class="py-3 px-4 font-semibold text-right">Ações</th>
              </tr>
            </thead>
            <tbody id="tabela-registros" class="divide-y divide-slate-100 text-sm">
              <!-- Linhas inseridas via JS -->
            </tbody>
          </table>
        </div>
      </div>
    </section>

    <!-- ABA 2: GRÁFICOS E RELATÓRIOS -->
    <section id="aba-graficos" class="hidden space-y-6">

      <!-- KPIs Gerais -->
      <div class="grid grid-cols-1 sm:grid-cols-3 gap-4">
        <div class="bg-white p-5 rounded-xl border border-slate-200 shadow-sm">
          <p class="text-xs font-medium text-slate-500 uppercase">Total de Presenças Registradas</p>
          <p id="kpi-total-presencas" class="text-3xl font-bold text-slate-800 mt-1">0</p>
        </div>
        <div class="bg-white p-5 rounded-xl border border-slate-200 shadow-sm">
          <p class="text-xs font-medium text-slate-500 uppercase">Total de Cultos Realizados</p>
          <p id="kpi-total-cultos" class="text-3xl font-bold text-blue-600 mt-1">0</p>
        </div>
        <div class="bg-white p-5 rounded-xl border border-slate-200 shadow-sm">
          <p class="text-xs font-medium text-slate-500 uppercase">Média de Pessoas por Culto</p>
          <p id="kpi-media-culto" class="text-3xl font-bold text-emerald-600 mt-1">0</p>
        </div>
      </div>

      <!-- Gráfico Principal: Frequência Temporal (Dia, Semana, Mês, Ano) -->
      <div class="bg-white p-6 rounded-xl border border-slate-200 shadow-sm">
        <div class="flex flex-col sm:flex-row justify-between items-start sm:items-center gap-4 mb-6">
          <div>
            <h3 class="text-lg font-bold text-slate-800">Evolução de Frequência</h3>
            <p class="text-xs text-slate-500">Quantidade de pessoas presentes agrupadas por período</p>
          </div>

          <div class="flex flex-wrap items-center gap-2">
            <!-- Seletor de Período -->
            <div class="inline-flex rounded-lg bg-slate-100 p-1">
              <button onclick="alterarPeriodoGrafico('dia')" id="btn-periodo-dia" class="px-3 py-1.5 text-xs font-semibold rounded-md bg-white text-blue-600 shadow-sm transition">Por Dia</button>
              <button onclick="alterarPeriodoGrafico('semana')" id="btn-periodo-semana" class="px-3 py-1.5 text-xs font-medium rounded-md text-slate-600 hover:text-slate-900 transition">Por Semana</button>
              <button onclick="alterarPeriodoGrafico('mes')" id="btn-periodo-mes" class="px-3 py-1.5 text-xs font-medium rounded-md text-slate-600 hover:text-slate-900 transition">Por Mês</button>
              <button onclick="alterarPeriodoGrafico('ano')" id="btn-periodo-ano" class="px-3 py-1.5 text-xs font-medium rounded-md text-slate-600 hover:text-slate-900 transition">Por Ano</button>
            </div>

            <!-- Filtro de Unção no Gráfico -->
            <select id="grafico-filtro-uncao" onchange="atualizarGraficos()" class="rounded-lg border border-slate-300 px-3 py-1.5 text-xs bg-white font-medium">
              <option value="TODOS">Todas as Unções</option>
              <option value="Bispo">Apenas Bispos</option>
              <option value="Pastor">Apenas Pastores</option>
              <option value="Presbítero">Apenas Presbíteros</option>
              <option value="Diácono">Apenas Diáconos</option>
              <option value="Aspirante">Apenas Aspirantes</option>
              <option value="Oficial">Apenas Oficiais</option>
              <option value="Membro">Apenas Membros</option>
              <option value="Visitante">Apenas Visitantes</option>
            </select>
          </div>
        </div>

        <div class="relative h-80 w-full">
          <canvas id="chart-temporal"></canvas>
        </div>
      </div>

      <!-- Gráficos Secundários: Por Unção e Por Ministério -->
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-6">
        <!-- Por Unção -->
        <div class="bg-white p-6 rounded-xl border border-slate-200 shadow-sm">
          <h3 class="text-base font-bold text-slate-800 mb-1">Distribuição por Unção</h3>
          <p class="text-xs text-slate-500 mb-4">Total acumulado por cargo ministerial</p>
          <div class="relative h-72 w-full">
            <canvas id="chart-uncao"></canvas>
          </div>
        </div>

        <!-- Por Ministério -->
        <div class="bg-white p-6 rounded-xl border border-slate-200 shadow-sm">
          <h3 class="text-base font-bold text-slate-800 mb-1">Participação por Ministério</h3>
          <p class="text-xs text-slate-500 mb-4">Presenças registradas em cada departamento</p>
          <div class="relative h-72 w-full">
            <canvas id="chart-ministerio"></canvas>
          </div>
        </div>
      </div>

    </section>

  </main>

  <script>
    // ==========================================
    // ESTADO E CONFIGURAÇÕES INICIAIS
    // ==========================================
    const STORAGE_KEY = 'igreja_controle_presenca_v1';
    const UNCOES_ORDEM = ['Bispo', 'Pastor', 'Presbítero', 'Diácono', 'Aspirante', 'Oficial', 'Membro', 'Visitante'];
    const CORES_UNCAO = {
      'Bispo': '#7c3aed',
      'Pastor': '#2563eb',
      'Presbítero': '#0284c7',
      'Diácono': '#0d9488',
      'Aspirante': '#16a34a',
      'Oficial': '#ca8a04',
      'Membro': '#475569',
      'Visitante': '#e11d48'
    };

    let registros = [];
    let periodoAtual = 'dia';
    let chartTemporal = null;
    let chartUncao = null;
    let chartMinisterio = null;

    // Inicialização ao carregar a página
    document.addEventListener('DOMContentLoaded', () => {
      lucide.createIcons();
      definirDataHoje();
      carregarDados();
      renderizarTudo();
    });

    function definirDataHoje() {
      const hoje = new Date().toISOString().split('T')[0];
      document.getElementById('input-data').value = hoje;
    }

    // ==========================================
    // ARMAZENAMENTO (LOCALSTORAGE)
    // ==========================================
    function carregarDados() {
      const salvos = localStorage.getItem(STORAGE_KEY);
      if (salvos) {
        registros = JSON.parse(salvos);
      } else {
        // Dados de exemplo iniciais para visualização imediata
        const hoje = new Date();
        const d1 = new Date(hoje); d1.setDate(hoje.getDate() - 14);
        const d2 = new Date(hoje); d2.setDate(hoje.getDate() - 7);
        const f = (dt) => dt.toISOString().split('T')[0];

        registros = [
          { id: 1, data: f(d1), culto: 'Culto de Domingo (Noite)', nome: 'Pr. Carlos Alberto', uncao: 'Pastor', ministerio: 'Geral / Sem Ministério' },
          { id: 2, data: f(d1), culto: 'Culto de Domingo (Noite)', nome: 'Pb. Marcos Vinícius', uncao: 'Presbítero', ministerio: 'Ensino / EBD' },
          { id: 3, data: f(d1), culto: 'Culto de Domingo (Noite)', nome: 'Dc. Roberto Silva', uncao: 'Diácono', ministerio: 'Recepção / Diaconato' },
          { id: 4, data: f(d1), culto: 'Culto de Domingo (Noite)', nome: 'Ana Paula Souza', uncao: 'Membro', ministerio: 'Louvor e Adoração' },
          { id: 5, data: f(d2), culto: 'Culto de Domingo (Noite)', nome: 'Bp. Antônio Ferreira', uncao: 'Bispo', ministerio: 'Geral / Sem Ministério' },
          { id: 6, data: f(d2), culto: 'Culto de Domingo (Noite)', nome: 'Asp. Lucas Mendes', uncao: 'Aspirante', ministerio: 'Jovens' },
          { id: 7, data: f(d2), culto: 'Culto de Domingo (Noite)', nome: 'Of. Juliana Costa', uncao: 'Oficial', ministerio: 'Infantil (Kids)' },
          { id: 8, data: f(hoje), culto: 'Culto de Domingo (Noite)', nome: 'Pr. Carlos Alberto', uncao: 'Pastor', ministerio: 'Geral / Sem Ministério' },
          { id: 9, data: f(hoje), culto: 'Culto de Domingo (Noite)', nome: 'Mariana Oliveira', uncao: 'Membro', ministerio: 'Mídia e Som' }
        ];
        salvarDados();
      }
    }

    function salvarDados() {
      localStorage.setItem(STORAGE_KEY, JSON.stringify(registros));
      atualizarDatalistPessoas();
    }

    // ==========================================
    // CRUD DE PRESENÇA
    // ==========================================
    function adicionarRegistro(event) {
      event.preventDefault();

      const data = document.getElementById('input-data').value;
      const culto = document.getElementById('input-culto').value;
      const nome = document.getElementById('input-nome').value.trim();
      const uncao = document.getElementById('input-uncao').value;
      const ministerio = document.getElementById('input-ministerio').value.trim() || 'Geral / Sem Ministério';

      if (!data || !nome) return;

      const novoRegistro = {
        id: Date.now(),
        data,
        culto,
        nome,
        uncao,
        ministerio
      };

      registros.unshift(novoRegistro);
      salvarDados();
      renderizarTudo();

      // Limpa apenas o nome para agilizar o próximo lançamento
      const inputNome = document.getElementById('input-nome');
      inputNome.value = '';
      inputNome.focus();
    }

    function removerRegistro(id) {
      if (confirm('Deseja remover este registro de presença?')) {
        registros = registros.filter(r => r.id !== id);
        salvarDados();
        renderizarTudo();
      }
    }

    function limparTodosDados() {
      if (confirm('ATENÇÃO: Isso apagará todos os registros salvos no navegador. Deseja continuar?')) {
        registros = [];
        salvarDados();
        renderizarTudo();
      }
    }

    // Autocompletar unção e ministério de pessoas já cadastradas anteriormente
    function atualizarDatalistPessoas() {
      const datalist = document.getElementById('lista-nomes-salvos');
      const nomesUnicos = [...new Set(registros.map(r => r.nome))].sort();
      datalist.innerHTML = nomesUnicos.map(nome => `<option value="${nome}">`).join('');
    }

    function autocompletarDadosPessoa(nomeDigitado) {
      const encontrado = registros.find(r => r.nome.toLowerCase() === nomeDigitado.trim().toLowerCase());
      if (encontrado) {
        document.getElementById('input-uncao').value = encontrado.uncao;
        document.getElementById('input-ministerio').value = encontrado.ministerio;
      }
    }

    // ==========================================
    // RENDERIZAÇÃO DA INTERFACE E TABELA
    // ==========================================
    function obterRegistrosFiltrados() {
      const fData = document.getElementById('filtro-data').value;
      const fUncao = document.getElementById('filtro-uncao').value;
      const fMin = document.getElementById('filtro-ministerio').value.toLowerCase();
      const fNome = document.getElementById('filtro-nome').value.toLowerCase();

      return registros.filter(r => {
        const matchData = !fData || r.data === fData;
        const matchUncao = !fUncao || r.uncao === fUncao;
        const matchMin = !fMin || r.ministerio.toLowerCase().includes(fMin);
        const matchNome = !fNome || r.nome.toLowerCase().includes(fNome);
        return matchData && matchUncao && matchMin && matchNome;
      });
    }

    function limparFiltros() {
      document.getElementById('filtro-data').value = '';
      document.getElementById('filtro-uncao').value = '';
      document.getElementById('filtro-ministerio').value = '';
      document.getElementById('filtro-nome').value = '';
      renderizarTudo();
    }

    function renderizarTudo() {
      const filtrados = obterRegistrosFiltrados();
      renderizarCardsUncao(filtrados);
      renderizarTabela(filtrados);
      atualizarDatalistPessoas();

      if (!document.getElementById('aba-graficos').classList.contains('hidden')) {
        atualizarGraficos();
      }
    }

    function renderizarCardsUncao(lista) {
      const container = document.getElementById('cards-uncao');
      container.innerHTML = UNCOES_ORDEM.map(uncao => {
        const qtd = lista.filter(r => r.uncao === uncao).length;
        const cor = CORES_UNCAO[uncao] || '#475569';
        return `
          <div onclick="filtrarRapidoUncao('${uncao}')" class="bg-white rounded-xl p-3 border border-slate-200 shadow-sm hover:border-blue-400 cursor-pointer transition">
            <div class="flex items-center justify-between">
              <span class="text-xs font-semibold text-slate-500">${uncao}</span>
              <span class="w-2.5 h-2.5 rounded-full" style="background-color: ${cor}"></span>
            </div>
            <p class="text-xl font-bold text-slate-800 mt-1">${qtd}</p>
          </div>
        `;
      }).join('');
    }

    function filtrarRapidoUncao(uncao) {
      const select = document.getElementById('filtro-uncao');
      select.value = select.value === uncao ? '' : uncao;
      renderizarTudo();
    }

    function renderizarTabela(lista) {
      const tbody = document.getElementById('tabela-registros');
      document.getElementById('contador-filtrado').textContent = lista.length;

      if (lista.length === 0) {
        tbody.innerHTML = `
          <tr>
            <td colspan="6" class="py-8 text-center text-slate-400 text-sm">
              Nenhum registro encontrado para os filtros selecionados.
            </td>
          </tr>
        `;
        return;
      }

      // Ordena da data mais recente para a mais antiga
      const ordenados = [...lista].sort((a, b) => b.data.localeCompare(a.data) || b.id - a.id);

      tbody.innerHTML = ordenados.map(r => {
        const [ano, mes, dia] = r.data.split('-');
        const dataFormatada = `${dia}/${mes}/${ano}`;
        const cor = CORES_UNCAO[r.uncao] || '#475569';

        return `
          <tr class="hover:bg-slate-50 transition">
            <td class="py-3 px-4 font-medium text-slate-700 whitespace-nowrap">${dataFormatada}</td>
            <td class="py-3 px-4 text-slate-600">${r.culto}</td>
            <td class="py-3 px-4 font-semibold text-slate-800">${r.nome}</td>
            <td class="py-3 px-4">
              <span class="inline-flex items-center px-2.5 py-0.5 rounded-full text-xs font-medium text-white" style="background-color: ${cor}">
                ${r.uncao}
              </span>
            </td>
            <td class="py-3 px-4 text-slate-600">${r.ministerio}</td>
            <td class="py-3 px-4 text-right">
              <button onclick="removerRegistro(${r.id})" title="Excluir" class="text-slate-400 hover:text-red-600 p-1 rounded transition">
                <i data-lucide="trash-2" class="w-4 h-4"></i>
              </button>
            </td>
          </tr>
        `;
      }).join('');

      lucide.createIcons();
    }

    // ==========================================
    // NAVEGAÇÃO ENTRE ABAS
    // ==========================================
    function mudarAba(aba) {
      const secRegistro = document.getElementById('aba-registro');
      const secGraficos = document.getElementById('aba-graficos');
      const btnRegistro = document.getElementById('btn-tab-registro');
      const btnGraficos = document.getElementById('btn-tab-graficos');

      if (aba === 'registro') {
        secRegistro.classList.remove('hidden');
        secGraficos.classList.add('hidden');
        btnRegistro.classList.add('tab-active');
        btnRegistro.classList.remove('text-slate-500');
        btnGraficos.classList.remove('tab-active');
        btnGraficos.classList.add('text-slate-500');
      } else {
        secRegistro.classList.add('hidden');
        secGraficos.classList.remove('hidden');
        btnGraficos.classList.add('tab-active');
        btnGraficos.classList.remove('text-slate-500');
        btnRegistro.classList.remove('tab-active');
        btnRegistro.classList.add('text-slate-500');
        atualizarGraficos();
      }
    }

    // ==========================================
    // GRÁFICOS (DIA, SEMANA, MÊS, ANO, UNÇÃO, MINISTÉRIO)
    // ==========================================
    function alterarPeriodoGrafico(novoPeriodo) {
      periodoAtual = novoPeriodo;
      ['dia', 'semana', 'mes', 'ano'].forEach(p => {
        const btn = document.getElementById(`btn-periodo-${p}`);
        if (p === novoPeriodo) {
          btn.className = 'px-3 py-1.5 text-xs font-semibold rounded-md bg-white text-blue-600 shadow-sm transition';
        } else {
          btn.className = 'px-3 py-1.5 text-xs font-medium rounded-md text-slate-600 hover:text-slate-900 transition';
        }
      });
      atualizarGraficos();
    }

    // Calcula número da semana ISO no ano
    function obterSemanaAno(dataStr) {
      const [ano, mes, dia] = dataStr.split('-').map(Number);
      const data = new Date(Date.UTC(ano, mes - 1, dia));
      const diaSemana = data.getUTCDay() || 7;
      data.setUTCDate(data.getUTCDate() + 4 - diaSemana);
      const inicioAno = new Date(Date.UTC(data.getUTCFullYear(), 0, 1));
      const semana = Math.ceil((((data - inicioAno) / 86400000) + 1) / 7);
      return `${data.getUTCFullYear()}-S${String(semana).padStart(2, '0')}`;
    }

    function atualizarGraficos() {
      // KPIs Gerais
      const totalPresencas = registros.length;
      const cultosUnicos = new Set(registros.map(r => `${r.data}_${r.culto}`)).size;
      const mediaCulto = cultosUnicos > 0 ? (totalPresencas / cultosUnicos).toFixed(1) : 0;

      document.getElementById('kpi-total-presencas').textContent = totalPresencas;
      document.getElementById('kpi-total-cultos').textContent = cultosUnicos;
      document.getElementById('kpi-media-culto').textContent = mediaCulto;

      // 1. Dados do Gráfico Temporal
      const filtroUncao = document.getElementById('grafico-filtro-uncao').value;
      const baseTemporal = filtroUncao === 'TODOS'
        ? registros
        : registros.filter(r => r.uncao === filtroUncao);

      const agrupado = {};
      baseTemporal.forEach(r => {
        let chave = r.data;
        if (periodoAtual === 'semana') {
          chave = obterSemanaAno(r.data);
        } else if (periodoAtual === 'mes') {
          chave = r.data.substring(0, 7); // YYYY-MM
        } else if (periodoAtual === 'ano') {
          chave = r.data.substring(0, 4); // YYYY
        }
        agrupado[chave] = (agrupado[chave] || 0) + 1;
      });

      const chavesOrdenadas = Object.keys(agrupado).sort();
      const labelsFormatados = chavesOrdenadas.map(chave => {
        if (periodoAtual === 'dia') {
          const [a, m, d] = chave.split('-');
          return `${d}/${m}/${a}`;
        }
        if (periodoAtual === 'mes') {
          const [a, m] = chave.split('-');
          return `${m}/${a}`;
        }
        if (periodoAtual === 'semana') {
          const [a, s] = chave.split('-');
          return `Sem ${s.replace('S', '')} (${a})`;
        }
        return chave;
      });
      const valoresTemporais = chavesOrdenadas.map(k => agrupado[k]);

      if (chartTemporal) chartTemporal.destroy();
      const ctxTemp = document.getElementById('chart-temporal').getContext('2d');
      chartTemporal = new Chart(ctxTemp, {
        type: 'bar',
        data: {
          labels: labelsFormatados,
          datasets: [{
            label: `Presenças (${filtroUncao === 'TODOS' ? 'Geral' : filtroUncao})`,
            data: valoresTemporais,
            backgroundColor: '#2563eb',
            borderRadius: 6,
            maxBarThickness: 48
          }]
        },
        options: {
          responsive: true,
          maintainAspectRatio: false,
          plugins: {
            legend: { display: false }
          },
          scales: {
            y: {
              beginAtZero: true,
              ticks: { precision: 0 }
            }
          }
        }
      });

      // 2. Gráfico por Unção
      const contagemUncao = UNCOES_ORDEM.map(u => registros.filter(r => r.uncao === u).length);
      const coresUncaoArray = UNCOES_ORDEM.map(u => CORES_UNCAO[u]);

      if (chartUncao) chartUncao.destroy();
      const ctxUncao = document.getElementById('chart-uncao').getContext('2d');
      chartUncao = new Chart(ctxUncao, {
        type: 'doughnut',
        data: {
          labels: UNCOES_ORDEM,
          datasets: [{
            data: contagemUncao,
            backgroundColor: coresUncaoArray,
            borderWidth: 2,
            borderColor: '#ffffff'
          }]
        },
        options: {
          responsive: true,
          maintainAspectRatio: false,
          plugins: {
            legend: { position: 'right' }
          }
        }
      });

      // 3. Gráfico por Ministério
      const mapaMin = {};
      registros.forEach(r => {
        mapaMin[r.ministerio] = (mapaMin[r.ministerio] || 0) + 1;
      });
      const minOrdenados = Object.entries(mapaMin).sort((a, b) => b[1] - a[1]);

      if (chartMinisterio) chartMinisterio.destroy();
      const ctxMin = document.getElementById('chart-ministerio').getContext('2d');
      chartMinisterio = new Chart(ctxMin, {
        type: 'bar',
        data: {
          labels: minOrdenados.map(item => item[0]),
          datasets: [{
            label: 'Presenças',
            data: minOrdenados.map(item => item[1]),
            backgroundColor: '#0d9488',
            borderRadius: 6
          }]
        },
        options: {
          indexAxis: 'y',
          responsive: true,
          maintainAspectRatio: false,
          plugins: {
            legend: { display: false }
          },
          scales: {
            x: {
              beginAtZero: true,
              ticks: { precision: 0 }
            }
          }
        }
      });
    }

    // ==========================================
    // EXPORTAÇÃO E BACKUP (CSV & JSON)
    // ==========================================
    function exportarCSV() {
      if (registros.length === 0) {
        alert('Não há dados para exportar.');
        return;
      }
      const cabecalho = ['Data', 'Culto', 'Nome', 'Uncao', 'Ministerio'];
      const linhas = registros.map(r => [
        r.data,
        `"${r.culto}"`,
        `"${r.nome}"`,
        `"${r.uncao}"`,
        `"${r.ministerio}"`
      ].join(';'));

      const csvContent = '\uFEFF' + [cabecalho.join(';'), ...linhas].join('\n');
      const blob = new Blob([csvContent], { type: 'text/csv;charset=utf-8;' });
      const url = URL.createObjectURL(blob);
      const link = document.createElement('a');
      link.href = url;
      link.download = `presenca_igreja_${new Date().toISOString().split('T')[0]}.csv`;
      link.click();
    }

    function exportarJSON() {
      const blob = new Blob([JSON.stringify(registros, null, 2)], { type: 'application/json' });
      const url = URL.createObjectURL(blob);
      const link = document.createElement('a');
      link.href = url;
      link.download = `backup_igreja_${new Date().toISOString().split('T')[0]}.json`;
      link.click();
    }

    function importarJSON(event) {
      const file = event.target.files[0];
      if (!file) return;

      const reader = new FileReader();
      reader.onload = (e) => {
        try {
          const dadosImportados = JSON.parse(e.target.result);
          if (Array.isArray(dadosImportados)) {
            registros = dadosImportados;
            salvarDados();
            renderizarTudo();
            alert('Backup restaurado com sucesso!');
          } else {
            alert('Formato de arquivo inválido.');
          }
        } catch (err) {
          alert('Erro ao ler o arquivo JSON.');
        }
      };
      reader.readAsText(file);
    }
  </script>
</body>
</html>
