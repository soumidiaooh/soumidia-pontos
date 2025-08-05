# soumidia-pontos
Gestão de Pontos Comerciais SOUMidia 
<!DOCTYPE html>
<html lang="pt-BR" class="h-full">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Soumidia - Gestão de Pontos Comerciais</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/xlsx/0.18.5/xlsx.full.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf-autotable/3.5.23/jspdf.plugin.autotable.min.js"></script>
  <style>
    @media (max-width: 768px) {
      .mes-col { min-width: 80px; }
    }
    .status-cell {
      @apply h-12 flex items-center justify-center text-white text-xs font-bold rounded cursor-pointer transition;
    }
    .disponivel { @apply bg-green-500; }
    .em_negociacao { @apply bg-yellow-500 text-black; }
    .ocupado { @apply bg-red-500; }
    .permuta { @apply bg-blue-500; }
    .retirar { @apply bg-orange-500; }
    .instalar { @apply bg-gray-500; }
    .acao-btn {
      @apply w-8 h-8 flex items-center justify-center rounded-full text-white text-sm hover:opacity-90;
    }
    .edit-btn { @apply bg-blue-600; }
    .delete-btn { @apply bg-red-600; }
  </style>
</head>
<body class="bg-gray-100 font-sans h-full">

  <div class="container mx-auto p-4 max-w-7xl">

    <h1 class="text-3xl font-bold text-center text-blue-800 mb-6">Soumidia - Gestão de Pontos Comerciais</h1>

    <!-- Abas de Navegação -->
    <div class="flex border-b mb-6">
      <button id="tab-dashboard" class="px-4 py-2 font-semibold border-b-2 border-blue-600">Dashboard</button>
      <button id="tab-pontos" class="px-4 py-2 text-gray-600 hover:text-blue-600">Pontos Comerciais</button>
      <button id="tab-clientes" class="px-4 py-2 text-gray-600 hover:text-blue-600">Clientes</button>
    </div>

    <!-- Dashboard -->
    <div id="view-dashboard" class="view">
      <div class="grid grid-cols-2 sm:grid-cols-3 lg:grid-cols-6 gap-4 mb-6">
        <div class="bg-white p-4 rounded-lg shadow text-center">
          <h3 class="text-sm text-gray-500">Total Pontos</h3>
          <p class="text-2xl font-bold" id="total-pontos">0</p>
        </div>
        <div class="bg-white p-4 rounded-lg shadow text-center">
          <h3 class="text-sm text-gray-500">Disponíveis</h3>
          <p class="text-2xl font-bold text-green-600" id="disp-pontos">0</p>
        </div>
        <div class="bg-white p-4 rounded-lg shadow text-center">
          <h3 class="text-sm text-gray-500">Ocupados</h3>
          <p class="text-2xl font-bold text-red-600" id="ocu-pontos">0</p>
        </div>
        <div class="bg-white p-4 rounded-lg shadow text-center">
          <h3 class="text-sm text-gray-500">Em Negociação</h3>
          <p class="text-2xl font-bold text-yellow-600" id="neg-pontos">0</p>
        </div>
        <div class="bg-white p-4 rounded-lg shadow text-center">
          <h3 class="text-sm text-gray-500">Permuta</h3>
          <p class="text-2xl font-bold text-blue-600" id="perm-pontos">0</p>
        </div>
        <div class="bg-white p-4 rounded-lg shadow text-center">
          <h3 class="text-sm text-gray-500">Receita (Mês)</h3>
          <p class="text-2xl font-bold text-purple-600" id="receita-mes">R$ 0</p>
        </div>
      </div>

      <div class="bg-white p-4 rounded-lg shadow mb-6">
        <h2 class="text-lg font-semibold mb-3">Filtros</h2>
        <div class="grid grid-cols-1 md:grid-cols-4 gap-4">
          <select id="filtro-mes" class="border rounded p-2">
            <option value="">Todos os meses</option>
            <option value="jan">Janeiro</option>
            <option value="fev">Fevereiro</option>
            <!-- ... todos os meses -->
            <option value="dez">Dezembro</option>
          </select>
          <select id="filtro-status" class="border rounded p-2">
            <option value="">Todos os status</option>
            <option value="disponivel">Disponível</option>
            <option value="em_negociacao">Em Negociação</option>
            <option value="ocupado">Ocupado</option>
            <option value="permuta">Permuta</option>
            <option value="retirar">Retirar</option>
            <option value="instalar">Instalar</option>
          </select>
          <select id="filtro-cliente" class="border rounded p-2">
            <option value="">Todos os clientes</option>
          </select>
          <input type="text" id="busca" placeholder="Buscar endereço..." class="border rounded p-2" />
        </div>
        <div class="mt-4 flex flex-wrap gap-2">
          <button id="btn-novo-ponto" class="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700">+ Novo Ponto</button>
          <button id="btn-exportar-excel" class="bg-gray-600 text-white px-4 py-2 rounded hover:bg-gray-700">📊 Excel</button>
          <button id="btn-exportar-pdf" class="bg-red-600 text-white px-4 py-2 rounded hover:bg-red-700">📄 PDF</button>
        </div>
      </div>

      <div class="bg-white rounded-lg shadow overflow-hidden">
        <div class="overflow-x-auto">
          <table class="w-full table-auto">
            <thead class="bg-gray-200">
              <tr>
                <th class="px-4 py-2 w-64">Endereço</th>
                <th class="mes-col px-2 py-2">Jan</th>
                <th class="mes-col px-2 py-2">Fev</th>
                <th class="mes-col px-2 py-2">Mar</th>
                <th class="mes-col px-2 py-2">Abr</th>
                <th class="mes-col px-2 py-2">Mai</th>
                <th class="mes-col px-2 py-2">Jun</th>
                <th class="mes-col px-2 py-2">Jul</th>
                <th class="mes-col px-2 py-2">Ago</th>
                <th class="mes-col px-2 py-2">Set</th>
                <th class="mes-col px-2 py-2">Out</th>
                <th class="mes-col px-2 py-2">Nov</th>
                <th class="mes-col px-2 py-2">Dez</th>
              </tr>
            </thead>
            <tbody id="tabela-pontos"></tbody>
          </table>
        </div>
      </div>
    </div>

    <!-- Lista de Pontos Comerciais -->
    <div id="view-pontos" class="view hidden">
      <div class="flex justify-between items-center mb-4">
        <h2 class="text-2xl font-bold">Pontos Comerciais</h2>
        <button id="btn-novo-ponto-lista" class="bg-blue-600 text-white px-4 py-2 rounded">+ Novo Ponto</button>
      </div>
      <div class="bg-white rounded-lg shadow overflow-hidden">
        <table class="w-full table-auto">
          <thead class="bg-gray-200">
            <tr>
              <th class="px-4 py-2">Endereço</th>
              <th class="px-4 py-2">Complemento</th>
              <th class="px-4 py-2">Observações</th>
              <th class="px-4 py-2 w-20">Ações</th>
            </tr>
          </thead>
          <tbody id="lista-pontos"></tbody>
        </table>
      </div>
    </div>

    <!-- Lista de Clientes -->
    <div id="view-clientes" class="view hidden">
      <div class="flex justify-between items-center mb-4">
        <h2 class="text-2xl font-bold">Clientes</h2>
        <button id="btn-novo-cliente-lista" class="bg-green-600 text-white px-4 py-2 rounded">+ Novo Cliente</button>
      </div>
      <div class="bg-white rounded-lg shadow overflow-hidden">
        <table class="w-full table-auto">
          <thead class="bg-gray-200">
            <tr>
              <th class="px-4 py-2">Nome</th>
              <th class="px-4 py-2">Empresa</th>
              <th class="px-4 py-2">Valor (R$)</th>
              <th class="px-4 py-2 w-20">Ações</th>
            </tr>
          </thead>
          <tbody id="lista-clientes"></tbody>
        </table>
      </div>
    </div>

  </div>

  <!-- Modal de Edição de Célula -->
  <div id="modal" class="fixed inset-0 bg-black bg-opacity-50 hidden flex items-center justify-center p-4">
    <div class="bg-white rounded-lg p-6 w-full max-w-md">
      <h3 class="text-xl font-bold mb-4">Editar Status</h3>
      <p class="mb-2"><strong>Ponto:</strong> <span id="modal-endereco"></span></p>
      <p class="mb-4"><strong>Mês:</strong> <span id="modal-mes"></span></p>
      <label class="block mb-2">Status</label>
      <select id="modal-status" class="border rounded p-2 w-full mb-4">
        <option value="disponivel">Disponível</option>
        <option value="em_negociacao">Em Negociação</option>
        <option value="ocupado">Ocupado</option>
        <option value="permuta">Permuta</option>
        <option value="retirar">Retirar</option>
        <option value="instalar">Instalar</option>
      </select>
      <label class="block mb-2">Cliente</label>
      <select id="modal-cliente" class="border rounded p-2 w-full mb-4">
      </select>
      <div class="flex justify-end gap-2">
        <button id="modal-cancelar" class="px-4 py-2 border rounded hover:bg-gray-100">Cancelar</button>
        <button id="modal-salvar" class="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700">Salvar</button>
      </div>
    </div>
  </div>

  <!-- Modal de Formulário -->
  <div id="modal-form" class="fixed inset-0 bg-black bg-opacity-50 hidden flex items-center justify-center p-4">
    <div class="bg-white rounded-lg p-6 w-full max-w-lg">
      <h3 id="form-titulo" class="text-xl font-bold mb-4">Novo Ponto</h3>
      <form id="form-cadastro">
        <input type="hidden" id="form-id" />
        <input type="hidden" id="form-tipo" />
        
        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 mb-4">
          <div>
            <label class="block mb-1">Endereço</label>
            <input type="text" id="form-endereco" class="border rounded p-2 w-full" required />
          </div>
          <div>
            <label class="block mb-1">Complemento</label>
            <input type="text" id="form-complemento" class="border rounded p-2 w-full" />
          </div>
        </div>
        <div class="mb-4">
          <label class="block mb-1">Observações</label>
          <textarea id="form-observacoes" class="border rounded p-2 w-full" rows="2"></textarea>
        </div>

        <div id="form-cliente-fields" class="hidden grid grid-cols-1 md:grid-cols-2 gap-4">
          <div>
            <label class="block mb-1">Nome</label>
            <input type="text" id="form-nome" class="border rounded p-2 w-full" />
          </div>
          <div>
            <label class="block mb-1">Empresa</label>
            <input type="text" id="form-empresa" class="border rounded p-2 w-full" />
          </div>
          <div class="md:col-span-2">
            <label class="block mb-1">Valor Negociado (R$)</label>
            <input type="number" id="form-valor" class="border rounded p-2 w-full" step="0.01" />
          </div>
        </div>

        <div class="flex justify-end gap-2">
          <button type="button" id="form-cancelar" class="px-4 py-2 border rounded hover:bg-gray-100">Cancelar</button>
          <button type="submit" class="bg-blue-600 text-white px-4 py-2 rounded hover:bg-blue-700">Salvar</button>
        </div>
      </form>
    </div>
  </div>

  <script>
    let pontos = JSON.parse(localStorage.getItem('soumidia_pontos')) || [];
    let clientes = JSON.parse(localStorage.getItem('soumidia_clientes')) || [];

    const mesesAbrev = ['jan','fev','mar','abr','mai','jun','jul','ago','set','out','nov','dez'];
    const mesesNome = ['Janeiro','Fevereiro','Março','Abril','Maio','Junho','Julho','Agosto','Setembro','Outubro','Novembro','Dezembro'];

    function salvarDados() {
      localStorage.setItem('soumidia_pontos', JSON.stringify(pontos));
      localStorage.setItem('soumidia_clientes', JSON.stringify(clientes));
    }

    function atualizarFiltros() {
      const selectCliente = document.getElementById('filtro-cliente');
      selectCliente.innerHTML = '<option value="">Todos os clientes</option>';
      clientes.forEach(c => {
        const opt = document.createElement('option');
        opt.value = c.id;
        opt.textContent = c.nome + (c.empresa ? ` (${c.empresa})` : '');
        selectCliente.appendChild(opt);
      });
    }

    function renderizarTabela() {
      const tbody = document.getElementById('tabela-pontos');
      tbody.innerHTML = '';

      const filtroMes = document.getElementById('filtro-mes').value;
      const filtroStatus = document.getElementById('filtro-status').value;
      const filtroCliente = document.getElementById('filtro-cliente').value;
      const busca = document.getElementById('busca').value.toLowerCase();

      pontos.forEach(ponto => {
        let mostrar = true;
        let temMesFiltro = false;

        const tr = document.createElement('tr');
        const tdEnd = document.createElement('td');
        tdEnd.className = "px-4 py-2 font-medium border";
        tdEnd.textContent = ponto.endereco;
        tr.appendChild(tdEnd);

        mesesAbrev.forEach((mes, idx) => {
          const data = ponto.meses[mes] || { status: 'disponivel' };
          const status = data.status;
          const clienteId = data.clienteId;
          const cliente = clienteId ? clientes.find(c => c.id === clienteId) : null;

          if (filtroMes && mes !== filtroMes) temMesFiltro = true;
          if (filtroMes && mes === filtroMes && filtroStatus && status !== filtroStatus) mostrar = false;
          if (filtroMes && mes === filtroMes && filtroCliente && clienteId !== filtroCliente) mostrar = false;
          if (!filtroMes && filtroStatus && status !== filtroStatus) mostrar = false;
          if (busca && !ponto.endereco.toLowerCase().includes(busca)) mostrar = false;

          const td = document.createElement('td');
          td.className = `mes-col px-2 py-1 border status-cell ${status}`;
          td.dataset.pontoId = ponto.id;
          td.dataset.mes = mes;

          if (status !== 'disponivel' && cliente) {
            td.title = `${cliente.nome} - ${cliente.empresa || ''}`;
            td.textContent = cliente.nome.split(' ')[0];
          } else {
            td.textContent = status === 'disponivel' ? '✔️' : '...';
          }

          td.addEventListener('click', abrirModalEdicao);
          tr.appendChild(td);
        });

        if (mostrar || !temMesFiltro) {
          tbody.appendChild(tr);
        }
      });

      atualizarDashboard();
    }

    function atualizarDashboard() {
      const total = pontos.length;
      let disp = 0, ocu = 0, neg = 0, perm = 0;
      let receita = 0;
      const mesAtivo = document.getElementById('filtro-mes').value || 'jan';

      pontos.forEach(ponto => {
        const status = (ponto.meses[mesAtivo] || {}).status || 'disponivel';
        const clienteId = (ponto.meses[mesAtivo] || {}).clienteId;
        const cliente = clienteId ? clientes.find(c => c.id === clienteId) : null;

        switch (status) {
          case 'disponivel': disp++; break;
          case 'ocupado': ocu++; if (cliente) receita += cliente.valorNegociado || 0; break;
          case 'em_negociacao': neg++; break;
          case 'permuta': perm++; break;
        }
      });

      document.getElementById('total-pontos').textContent = total;
      document.getElementById('disp-pontos').textContent = disp;
      document.getElementById('ocu-pontos').textContent = ocu;
      document.getElementById('neg-pontos').textContent = neg;
      document.getElementById('perm-pontos').textContent = perm;
      document.getElementById('receita-mes').textContent = `R$ ${receita.toFixed(2)}`;
    }

    function renderizarListaPontos() {
      const tbody = document.getElementById('lista-pontos');
      tbody.innerHTML = '';
      pontos.forEach(ponto => {
        const tr = document.createElement('tr');
        tr.className = "border-t";
        tr.innerHTML = `
          <td class="px-4 py-2">${ponto.endereco}</td>
          <td class="px-4 py-2">${ponto.complemento || ''}</td>
          <td class="px-4 py-2">${ponto.observacoes || ''}</td>
          <td class="px-4 py-2 text-center">
            <button data-id="${ponto.id}" class="acao-btn edit-btn mr-1 editar-ponto">✏️</button>
            <button data-id="${ponto.id}" class="acao-btn delete-btn excluir-ponto">🗑️</button>
          </td>
        `;
        tbody.appendChild(tr);
      });
    }

    function renderizarListaClientes() {
      const tbody = document.getElementById('lista-clientes');
      tbody.innerHTML = '';
      clientes.forEach(cliente => {
        const tr = document.createElement('tr');
        tr.className = "border-t";
        tr.innerHTML = `
          <td class="px-4 py-2">${cliente.nome}</td>
          <td class="px-4 py-2">${cliente.empresa || ''}</td>
          <td class="px-4 py-2">R$ ${cliente.valorNegociado.toFixed(2)}</td>
          <td class="px-4 py-2 text-center">
            <button data-id="${cliente.id}" class="acao-btn edit-btn mr-1 editar-cliente">✏️</button>
            <button data-id="${cliente.id}" class="acao-btn delete-btn excluir-cliente">🗑️</button>
          </td>
        `;
        tbody.appendChild(tr);
      });
    }

    // --- MODAIS ---
    function abrirModalEdicao(e) {
      const pontoId = e.target.dataset.pontoId;
      const mes = e.target.dataset.mes;
      const ponto = pontos.find(p => p.id === pontoId);

      document.getElementById('modal-endereco').textContent = ponto.endereco;
      document.getElementById('modal-mes').textContent = mesesNome[mesesAbrev.indexOf(mes)];
      document.getElementById('modal-status').value = (ponto.meses[mes] || {}).status || 'disponivel';

      const selectCliente = document.getElementById('modal-cliente');
      selectCliente.innerHTML = '<option value="">Selecione...</option>';
      clientes.forEach(c => {
        const opt = document.createElement('option');
        opt.value = c.id;
        opt.textContent = c.nome + (c.empresa ? ` (${c.empresa})` : '');
        if ((ponto.meses[mes] || {}).clienteId === c.id) opt.selected = true;
        selectCliente.appendChild(opt);
      });

      document.getElementById('modal').classList.remove('hidden');
      window.modalData = { pontoId, mes };
    }

    document.getElementById('modal-cancelar').addEventListener('click', () => {
      document.getElementById('modal').classList.add('hidden');
    });

    document.getElementById('modal-salvar').addEventListener('click', () => {
      const { pontoId, mes } = window.modalData;
      const status = document.getElementById('modal-status').value;
      const clienteId = document.getElementById('modal-cliente').value || null;

      const ponto = pontos.find(p => p.id === pontoId);
      if (!ponto.meses[mes]) ponto.meses[mes] = {};
      ponto.meses[mes].status = status;
      if (status !== 'disponivel') ponto.meses[mes].clienteId = clienteId;
      else delete ponto.meses[mes].clienteId;

      salvarDados();
      renderizarTabela();
      document.getElementById('modal').classList.add('hidden');
      alert('Status atualizado com sucesso!');
    });

    // --- FORMULÁRIO ---
    function abrirFormulario(tipo, item = null) {
      document.getElementById('form-tipo').value = tipo;
      document.getElementById('form-cliente-fields').classList.toggle('hidden', tipo !== 'cliente');
      document.getElementById('form-titulo').textContent = tipo === 'ponto' ? 'Editar Ponto Comercial' : 'Editar Cliente';

      if (item) {
        document.getElementById('form-id').value = item.id;
        if (tipo === 'ponto') {
          document.getElementById('form-endereco').value = item.endereco;
          document.getElementById('form-complemento').value = item.complemento || '';
          document.getElementById('form-observacoes').value = item.observacoes || '';
        } else {
          document.getElementById('form-nome').value = item.nome;
          document.getElementById('form-empresa').value = item.empresa || '';
          document.getElementById('form-valor').value = item.valorNegociado || '';
        }
      } else {
        document.getElementById('form-cadastro').reset();
        document.ge
