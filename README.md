<!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Feature: Modo Daltonismo</title>

  <!--
    Ideia da página:
    - Coluna esquerda: cores originais do site
    - Coluna direita: versões acessíveis (daltonismo)
    - Botão para alternar o modo (simulando a feature)
    - Pensada para GitHub Pages (HTML + CSS + JS puro)
  -->

  <style>
    :root {
      /* Cores originais */
      --primary: #0057ff;
      --secondary: #ff4d4f;
      --background: #ffffff;
      --text: #1f2937;

      /* Cores acessíveis (daltonismo) */
      --primary-accessible: #1b9e77;   /* verde azulado */
      --secondary-accessible: #d95f02; /* laranja */
      --background-accessible: #f9fafb;
      --text-accessible: #111827;
    }

    body {
      margin: 0;
      font-family: system-ui, -apple-system, BlinkMacSystemFont, "Segoe UI", sans-serif;
      background: var(--background);
      color: var(--text);
    }

    header {
      padding: 24px;
      border-bottom: 1px solid #e5e7eb;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    header h1 {
      margin: 0;
      font-size: 1.5rem;
    }

    button {
      padding: 10px 16px;
      font-size: 0.9rem;
      border-radius: 8px;
      border: none;
      cursor: pointer;
      background: var(--primary);
      color: #fff;
      transition: background 0.2s ease;
    }

    button:hover {
      opacity: 0.9;
    }

    main {
      display: grid;
      grid-template-columns: 1fr 1fr;
      min-height: calc(100vh - 80px);
    }

    .column {
      padding: 32px;
    }

    .column h2 {
      margin-top: 0;
      font-size: 1.25rem;
    }

    .card {
      border-radius: 12px;
      padding: 20px;
      margin-bottom: 16px;
      background: #f3f4f6;
    }

    .color-box {
      height: 48px;
      border-radius: 8px;
      margin-top: 8px;
    }

    /* Coluna original */
    .original .primary {
      background: var(--primary);
    }

    .original .secondary {
      background: var(--secondary);
    }

    /* Coluna acessível */
    .accessible {
      background: var(--background-accessible);
      color: var(--text-accessible);
    }

    .accessible .card {
      background: #ffffff;
      border: 1px solid #e5e7eb;
    }

    .accessible .primary {
      background: var(--primary-accessible);
    }

    .accessible .secondary {
      background: var(--secondary-accessible);
    }

    /* Modo acessível ativado (simulação do botão no site real) */
    body.accessible-mode {
      background: var(--background-accessible);
      color: var(--text-accessible);
    }

    body.accessible-mode button {
      background: var(--primary-accessible);
    }

    footer {
      padding: 16px;
      text-align: center;
      font-size: 0.85rem;
      color: #6b7280;
    }
  </style>
</head>
<body>

  <header>
    <h1>Feature: Modo Daltonismo 🎨</h1>
    <button onclick="toggleAccessibleMode()">Alternar modo acessível</button>
  </header>

  <main>
    <!-- Coluna esquerda: cores originais -->
    <section class="column original">
      <h2>Cores Originais</h2>

      <div class="card">
        <strong>Cor Primária</strong>
        <div class="color-box primary"></div>
      </div>

      <div class="card">
        <strong>Cor Secundária</strong>
        <div class="color-box secondary"></div>
      </div>

      <p>
        Este é o esquema de cores atual do site.
        Para pessoas com daltonismo, algumas combinações podem ter baixo contraste
        ou serem difíceis de diferenciar.
      </p>
    </section>

    <!-- Coluna direita: cores acessíveis -->
    <section class="column accessible">
      <h2>Cores Acessíveis (Daltonismo)</h2>

      <div class="card">
        <strong>Cor Primária (Acessível)</strong>
        <div class="color-box primary"></div>
      </div>

      <div class="card">
        <strong>Cor Secundária (Acessível)</strong>
        <div class="color-box secondary"></div>
      </div>

      <p>
        Paleta ajustada para melhor contraste e distinção de cores,
        considerando principalmente deuteranopia e protanopia.
      </p>
    </section>
  </main>

  <footer>
    Demo para apresentação de feature de acessibilidade • GitHub Pages
  </footer>

  <script>
    function toggleAccessibleMode() {
      document.body.classList.toggle('accessible-mode');
    }
  </script>

</body>
</html>