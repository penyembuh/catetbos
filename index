<!doctype html>
<html lang="id">
<head>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600;700&display=swap" rel="stylesheet">
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Catatan Keuangan</title>
  <style>
    :root{
      /* Tema: Blue (dark + blue accent) */
      --bg1:#0B1020;
      --bg2:#070A12;

      --card:rgba(255,255,255,.06);
      --stroke:rgba(255,255,255,.10);
      --text:rgba(255,255,255,.92);
      --muted:rgba(255,255,255,.68);
      --shadow:0 18px 40px rgba(0,0,0,.45);
      --radius:18px;

      --accent:#3B82F6;        /* Blue 500 */
      --accent2:#60A5FA;       /* Blue 400 */
      --accentSoft: rgba(59,130,246,.16);
      --accentGlow1: rgba(59,130,246,.22);
      --accentGlow2: rgba(96,165,250,.16);
      --accentRing: rgba(59,130,246,.14);
      --accentBorder: rgba(59,130,246,.44);
      --accentBorderSoft: rgba(59,130,246,.35);
      --accentDot: rgba(59,130,246,.92);
      --accentDot2: rgba(96,165,250,.92);
    }
    *{box-sizing:border-box}

    body{
      margin:0;
      font-family:'Plus Jakarta Sans', ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Arial;
      color:var(--text);
      background:
        radial-gradient(900px 560px at 12% 10%, var(--accentGlow1), transparent 58%),
        radial-gradient(860px 520px at 88% 18%, var(--accentGlow2), transparent 62%),
        radial-gradient(980px 560px at 50% 110%, rgba(255,255,255,.06), transparent 62%),
        linear-gradient(180deg, var(--bg1), var(--bg2));
      min-height:100vh;
      padding:calc(env(safe-area-inset-top) + 14px) 10px calc(env(safe-area-inset-bottom) + 22px);
    }

    .viewport{width:100%;display:flex;justify-content:stretch}
    .wrap{max-width:520px;width:100%;margin:0 auto}

    header{
      display:flex;align-items:center;justify-content:space-between;gap:14px;
      margin-bottom:14px;
      flex-wrap:wrap;
      padding:0 2px;
    }

    .brand{display:flex;align-items:center;gap:12px}
    /* Logo image (PNG/SVG via URL) */
    .logo-img{
      width:40px;
      height:40px;
      border-radius:13px; /* ubah ke 0 jika mau kotak */
      object-fit:contain;
      background:rgba(255,255,255,.08);
      border:1px solid rgba(255,255,255,.18);
      box-shadow: 0 10px 25px rgba(0,0,0,.35);
    }

    h1{font-size:20px;margin:0;letter-spacing:.2px}
    .sub{color:var(--muted);font-size:12px;margin-top:2px}

    .toolbar{
      width:100%;
      display:grid;
      grid-template-columns: repeat(5, minmax(0, 1fr));
      gap:8px;
      align-items:stretch;
    }
    .toolbar .btn{
      width:100%;
      padding:10px 10px;
      font-size:12px;
      line-height:1.1;
      border-radius:14px;
      min-height:42px;
      justify-content:center;
    }

    .grid{display:grid;gap:12px}

    .card{
      background:linear-gradient(180deg, var(--card), rgba(255,255,255,.05));
      border:1px solid var(--stroke);
      border-radius:var(--radius);
      box-shadow:var(--shadow);
      overflow:hidden;
    }
    .card .head{
      padding:12px 12px;
      display:flex;align-items:center;justify-content:space-between;gap:10px;
      border-bottom:1px solid rgba(255,255,255,.10);
      background:linear-gradient(180deg, rgba(255,255,255,.08), rgba(255,255,255,.02));
    }
    .card .head h3{margin:0;font-size:14px;letter-spacing:.3px}
    .badge{
      font-size:12px;color:var(--muted);
      padding:6px 10px;border-radius:999px;
      background:rgba(255,255,255,.07);
      border:1px solid rgba(255,255,255,.12);
      user-select:none;
    }
    .card .body{padding:14px 12px}

    .row{display:flex;gap:10px;flex-wrap:wrap}

    label{font-size:12px;color:var(--muted);display:block;margin:0 0 6px}

    .field{flex:1;min-width:160px}
    .field.sm{min-width:140px;flex:0 0 170px}

    input, select{
      width:100%;
      padding:11px 12px;
      border-radius:14px;
      border:1px solid rgba(255,255,255,.14);
      background:rgba(11,16,32,.35);
      color:var(--text);
      outline:none;
      box-shadow: inset 0 1px 0 rgba(255,255,255,.06);
    }
    input::placeholder{color:rgba(255,255,255,.45)}
    input:focus, select:focus{border-color:rgba(59,130,246,.55); box-shadow: 0 0 0 4px var(--accentRing)}

    .btn{
      padding:11px 14px;
      min-height:42px;
      border-radius:14px;
      border:1px solid rgba(255,255,255,.14);
      background:rgba(255,255,255,.08);
      color:var(--text);
      cursor:pointer;
      transition: transform .12s ease, background .12s ease, border-color .12s ease;
      user-select:none;
      white-space:nowrap;
      display:inline-flex;
      align-items:center;
      justify-content:center;
      gap:10px;
    }
    .btn:hover{transform: translateY(-1px); background:rgba(255,255,255,.12)}
    .btn:active{transform: translateY(0px)}

    .btn.primary{
      border-color: var(--accentBorderSoft);
      background: linear-gradient(135deg, rgba(59,130,246,.20), rgba(96,165,250,.12));
    }

    .btn.danger{
      border-color: rgba(248,113,113,.35);
      background: linear-gradient(135deg, rgba(248,113,113,.22), rgba(248,113,113,.10));
      color: rgba(255,255,255,.95);
      font-weight: 750;
    }

    .btn.ghost{background:transparent}

    /* add button (green – enhanced) */
    .btn.addGreen{
      position:relative;
      border-color: rgba(29,185,84,.65);
      background: linear-gradient(135deg, rgba(29,185,84,.45), rgba(29,185,84,.18));
      color: rgba(255,255,255,.98);
      font-weight: 850;
      padding:12px 14px;
      overflow:hidden;
      box-shadow:
        0 10px 25px rgba(29,185,84,.25),
        inset 0 1px 0 rgba(255,255,255,.25);
    }
    .btn.addGreen::before{
      content:"";
      position:absolute;
      inset:-40% -20% auto -20%;
      height:120%;
      background:linear-gradient(120deg, transparent 30%, rgba(255,255,255,.35), transparent 60%);
      transform:translateX(-100%);
      transition:transform .6s ease;
    }
    .btn.addGreen:hover::before{
      transform:translateX(120%);
    }
    .btn.addGreen:hover{
      background: linear-gradient(135deg, rgba(29,185,84,.55), rgba(29,185,84,.25));
      border-color: rgba(29,185,84,.8);
      transform: translateY(-2px) scale(1.01);
    }
    .btn.addGreen:active{
      transform: translateY(0) scale(.98);
    }
    .btn.addGreen .plus{
      width:36px;height:36px;
      border-radius:14px;
      display:grid;place-items:center;
      background: linear-gradient(135deg, rgba(29,185,84,.55), rgba(29,185,84,.25));
      border: 1px solid rgba(29,185,84,.45);
      box-shadow: inset 0 1px 0 rgba(255,255,255,.25);
    }
    .btn.addGreen svg{display:block}

    /* Floating Add Button (single source: #openAddTab) */
    #addBtnSlot{width:100%}
    .btn.fab{
      position:fixed;
      right:14px;
      bottom:calc(env(safe-area-inset-bottom) + 14px);
      z-index:1190;
      width:56px;
      height:56px;
      padding:0;
      border-radius:18px;
      box-shadow: 0 18px 45px rgba(0,0,0,.45);
    }
    .btn.fab .plus{width:40px;height:40px;border-radius:14px}
    .btn.fab span:last-child{display:none}

    .stats{
      display:grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap:10px;
    }
    .stat{
      padding:11px 10px;
      border-radius:16px;
      border:1px solid rgba(255,255,255,.12);
      background:rgba(255,255,255,.06);
      min-width:0;
    }
    .stat .k{font-size:11px;color:var(--muted);font-weight:650;letter-spacing:.15px}
    .stat .v{font-size:15px;font-weight:800;margin-top:6px;line-height:1.15;white-space:nowrap;overflow:hidden;text-overflow:ellipsis}

    @media (max-width:420px){
      .stats{grid-template-columns: repeat(2, minmax(0, 1fr));}
    }
    @media (max-width:320px){
      .stats{grid-template-columns: 1fr;}
      .stat .v{font-size:16px}
    }
    .pos{color:rgba(34,197,94,.95)}
    .neg{color:rgba(248,113,113,.95)}

    .chip{
      display:inline-flex;align-items:center;gap:8px;
      padding:6px 10px;border-radius:999px;
      border:1px solid rgba(255,255,255,.12);
      background:rgba(255,255,255,.06);
      font-size:12px;color:var(--muted);
      white-space:nowrap;
    }
    .dot{width:8px;height:8px;border-radius:999px;background:var(--accentDot)}
    .dot.exp{background:rgba(248,113,113,.9)}
    .dot.trf{background:var(--accentDot2)}

    .filters{display:flex;gap:8px;flex-wrap:nowrap;overflow-x:auto;-webkit-overflow-scrolling:touch;padding-bottom:6px;scroll-snap-type:x mandatory}
    .filters::-webkit-scrollbar{height:6px}
    .filters::-webkit-scrollbar-thumb{background:rgba(255,255,255,.12);border-radius:999px}
    .filterBtn{flex:0 0 auto; scroll-snap-align:start}

    .filterBtn{
      padding:8px 10px;
      border-radius:999px;
      border:1px solid rgba(255,255,255,.14);
      background:rgba(255,255,255,.06);
      color:var(--muted);
      cursor:pointer;
      font-weight:600;
      font-size:12px;
      transition: transform .12s ease, background .12s ease;
    }
    .filterBtn:hover{transform: translateY(-1px); background:rgba(255,255,255,.10)}
    .filterBtn.active{color:var(--text); border-color:rgba(59,130,246,.40); background:rgba(59,130,246,.14)}

    .txFilters{
      display:grid;
      grid-template-columns: 2fr 1fr;
      gap:10px;
      align-items:end;
    }
    .txFilters .field{min-width:0}

    @media (max-width:420px){
      .txFilters{grid-template-columns: 1fr;}
    }

    .miniStats{display:grid;grid-template-columns:repeat(2,1fr);gap:10px}
    @media (max-width:360px){.miniStats{grid-template-columns:1fr}}

    .miniStat{
      padding:10px 10px;
      border-radius:16px;
      border:1px solid rgba(255,255,255,.12);
      background:rgba(255,255,255,.05);
    }
    .miniStat .k{font-size:11px;color:var(--muted);font-weight:650;letter-spacing:.2px}
    .miniStat .v{font-size:13px;font-weight:750;margin-top:4px}

    .txList{display:flex;flex-direction:column;gap:12px}
    .txDay{border-radius:18px;border:1px solid rgba(255,255,255,.10);background:rgba(11,16,32,.20);overflow:hidden}
    .txDayHead{display:flex;align-items:center;justify-content:space-between;gap:10px;padding:10px 12px;background:rgba(255,255,255,.04);border-bottom:1px solid rgba(255,255,255,.08)}
    .txDayHead .d{font-size:12px;color:var(--muted);font-weight:650}
    .txDayHead .c{font-size:12px;color:var(--muted)}

    .txItem{display:flex;gap:10px;padding:12px;align-items:flex-start}
    .txItem + .txItem{border-top:1px solid rgba(255,255,255,.08)}
    .txMain{flex:1;min-width:0}
    .txTitle{display:flex;align-items:center;gap:8px;font-weight:750;font-size:13px}
    .txMeta{display:flex;flex-wrap:wrap;gap:8px;margin-top:6px}
    .txNote{margin-top:6px;font-size:12px;color:var(--muted);overflow:hidden;text-overflow:ellipsis;white-space:nowrap}

    .txItem{cursor:pointer;transition:background .12s ease}
    .txItem:hover{background:rgba(255,255,255,.02)}
    .txItem:active{background:rgba(255,255,255,.04)}

    .txRight{display:flex;flex-direction:column;align-items:flex-end;gap:6px;min-width:112px}
    .txAmt{font-weight:850;font-size:14px;letter-spacing:.2px}
    .txChevron{font-size:18px;line-height:1;color:rgba(255,255,255,.55)}

    .detailGrid{display:flex;flex-direction:column;gap:10px}
    .detailRow{display:flex;justify-content:space-between;gap:10px;align-items:flex-start;padding:10px 10px;border-radius:16px;border:1px solid rgba(255,255,255,.12);background:rgba(255,255,255,.05)}
    .detailRow .k{font-size:11px;color:var(--muted);font-weight:650;letter-spacing:.15px}
    .detailRow .v{font-size:13px;font-weight:750;text-align:right;max-width:68%;word-break:break-word}

    .txForm{
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap:12px;
    }
    .txForm .field{min-width:0}
    .txForm .col2{grid-column: 1 / -1}

    @media (max-width:340px){
      .txForm{grid-template-columns: 1fr;}
    }

    .modalMask{position:fixed;inset:0;background:rgba(0,0,0,.45);opacity:0;pointer-events:none;transition:opacity .18s ease;z-index:1200}
    .modalMask.show{opacity:1;pointer-events:auto}

    .modal{
      position:fixed;
      left:50%;
      bottom:16px;
      transform:translateX(-50%) translateY(16px);
      width:min(520px, calc(100vw - 22px));
      background:linear-gradient(180deg, rgba(18,27,51,.95), rgba(11,16,32,.95));
      border:1px solid rgba(255,255,255,.14);
      border-radius:22px;
      box-shadow:0 24px 60px rgba(0,0,0,.55);
      padding:12px 12px 12px;
      opacity:0;
      pointer-events:none;
      transition:opacity .18s ease, transform .18s ease;
      z-index:1201;
      max-height: calc(100vh - 24px - env(safe-area-inset-top));
      overflow:auto;
    }
    .modal.show{opacity:1;pointer-events:auto; transform:translateX(-50%) translateY(0)}

    .modalHead{display:flex;align-items:center;justify-content:space-between;gap:10px;padding:4px 4px 10px}
    .modalHead h3{margin:0;font-size:14px;letter-spacing:.2px}
    .modalBody{padding:0 4px 4px}

    .accTypeRow{
      display:flex;gap:10px;align-items:center;flex-wrap:wrap;
      padding:10px 10px;
      border-radius:16px;
      border:1px solid rgba(255,255,255,.12);
      background:rgba(255,255,255,.06);
      margin-bottom:10px;
    }
    .accTypeMeta{font-size:11px;color:var(--muted);flex:1 0 100%}
    .accTypeRow input{
      flex:1;
      padding:10px 10px;
      border-radius:14px;
      border:1px solid rgba(255,255,255,.14);
      background:rgba(11,16,32,.35);
      color:var(--text);
    }
    .accTypeRow input.emojiIn{flex:0 0 64px;min-width:64px;text-align:center;font-size:18px;padding:10px 6px}
    .accTypeRow .num{flex:1 0 100%;min-width:100%;text-align:right}

    .iconMini{width:42px;height:42px;border-radius:14px;border:1px solid rgba(255,255,255,.14);background:rgba(255,255,255,.08);color:var(--text);cursor:pointer}
    .modalFooter{
      display:grid;
      grid-template-columns: 1fr 1fr;
      gap:10px;
      padding:4px;
    }
    .modalFooter .btn{width:100%}

    .sp6{height:6px}
    .sp10{height:10px}
    .sp12{height:12px}
    .sp14{height:14px}

    @media (max-width:360px){
      .toolbar{grid-template-columns: 1fr 1fr;}
      .toolbar .btn{font-size:12px}
      .txRight{min-width:98px}
    }

    .toast{
      position:fixed;left:50%;bottom:18px;transform:translateX(-50%);
      padding:10px 12px;border-radius:14px;
      background:rgba(0,0,0,.55);
      color:rgba(255,255,255,.92);
      border:1px solid rgba(255,255,255,.12);
      box-shadow:0 16px 30px rgba(0,0,0,.35);
      opacity:0; pointer-events:none;
      transition: opacity .18s ease, transform .18s ease;
      backdrop-filter: blur(10px);
      font-size:13px;
      z-index:999;
    }
    .toast.show{opacity:1; transform:translateX(-50%) translateY(-6px)}

    .muted{color:var(--muted)}
    .hint{font-size:12px;color:var(--muted);margin-top:10px}
    .hidden{display:none !important}

    /* helpers */
    .block{width:100%}

    /* ===== PIN Lock UI ===== */
    body.locked{overflow:hidden}
    .lockMask{position:fixed;inset:0;background:rgba(0,0,0,.62);opacity:0;pointer-events:none;transition:opacity .18s ease;z-index:3000}
    .lockMask.show{opacity:1;pointer-events:auto}
    .lock{
      position:fixed;
      left:50%;
      top:50%;
      transform:translate(-50%,-46%);
      width:min(520px, calc(100vw - 22px));
      background:linear-gradient(180deg, rgba(18,27,51,.96), rgba(11,16,32,.96));
      border:1px solid rgba(255,255,255,.14);
      border-radius:22px;
      box-shadow:0 24px 60px rgba(0,0,0,.6);
      opacity:0;
      pointer-events:none;
      transition:opacity .18s ease, transform .18s ease;
      z-index:3001;
      padding:12px;
    }
    .lock.show{opacity:1;pointer-events:auto;transform:translate(-50%,-50%)}
    .lockHead{padding:8px 8px 4px}
    .lockTitle{font-size:16px;font-weight:850;letter-spacing:.2px}
    .lockSub{font-size:12px;color:var(--muted);margin-top:4px;line-height:1.35}
    .lockBody{padding:10px 8px 6px}
    .lockActions{display:grid;grid-template-columns:1fr 1fr;gap:10px}
    .lockActions.three{grid-template-columns:1fr 1fr 1fr}
    @media (max-width:360px){.lockActions.three{grid-template-columns:1fr}}
    @media (max-width:360px){.lockActions{grid-template-columns:1fr}}
  </style>
</head>
<body>
  <!-- PIN Lock Screen -->
  <div class="lockMask" id="lockMask" aria-hidden="true"></div>
  <div class="lock" id="lockModal" aria-hidden="true" role="dialog" aria-modal="true">
    <div class="lockHead">
      <div class="lockTitle">🔒 Login PIN</div>
      <div class="lockSub" id="lockSub">Masukkan PIN untuk membuka catatan keuangan.</div>
    </div>

    <div class="lockBody">
      <div class="field" style="min-width:0">
        <label for="pinInput">PIN</label>
        <input id="pinInput" type="password" inputmode="numeric" autocomplete="off" maxlength="12" placeholder="••••" />
        <div class="hint" id="pinHint" style="margin-top:10px"></div>
      </div>

      <div class="sp10"></div>

      <div class="lockActions">
        <button class="btn primary" id="pinSubmitBtn" type="button">Masuk</button>
        <button class="btn ghost" id="pinModeBtn" type="button">Set PIN</button>
        <button class="btn ghost hidden" id="pinTargetBtn" type="button" title="Pilih PIN yang ingin diatur">PIN: Utama</button>
      </div>

      <div class="sp10"></div>
      <button class="btn danger block hidden" id="pinResetAllBtn" type="button" title="Hapus semua data jika lupa PIN">Lupa PIN? Reset semua data</button>
      <div class="hint" style="margin-top:10px;line-height:1.4">
        Lupa PIN? Masukkan <b>Recovery PIN</b> untuk masuk. (Recovery PIN bisa kamu buat dari tombol <b>Set PIN</b> setelah berhasil login)
      </div>
    </div>
  </div>

  <div class="viewport">
    <div class="wrap hidden" id="appWrap">
      <header>
        <div class="brand">
          <!-- Logo: file harus berada di folder yang sama dengan HTML -->
          <!-- Logo PNG: pastikan file berada di folder yang sama dengan HTML -->
          <!-- Logo SVG: pastikan file berada di folder yang sama dengan HTML -->
          <!-- Logo SVG embedded (data URI) agar PASTI muncul di web tanpa file terpisah) -->
          <!-- Logo via URL (sesuai permintaan) -->
          <img class="logo-img" src="https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEh8XJ4onx_A7huo4jiwy0xhV62eh19dfRX1EFndQO3tfUP3yvS_CPJtZ3u2C-yLTgWywKBcCqtLYr2wny4gP_oRe44yAhuaZSwojo-VqyO1e8u-ssB6FabRxmp33AFyUDxSvl1ZRi6Q1rcZ87gGaSkn5vsWxrSzUKExjuN9m-dXtpKmC9kYrLPUX2SNVjw/s500/png%20my%20komuk.png" alt="Logo" />
          <div>
            <h1>Catatan Keuangan</h1>
            <div class="sub">Demo ringan • hitung pemasukan, pengeluaran, & transfer</div>
          </div>
        </div>

        <div class="toolbar">
          <button class="btn ghost" id="seedBtn" title="Isi contoh data">Isi contoh</button>
          <button class="btn ghost" id="resetBtn" title="Hapus semua transaksi">Reset</button>
          <button class="btn" id="exportBtn" title="Backup full: download semua transaksi ke spreadsheet (CSV)">Backup CSV</button>
          <button class="btn ghost" id="pinSettingsBtn" title="Ganti PIN / set Recovery PIN">PIN</button>
          <button class="btn ghost" id="logoutBtn" title="Kunci aplikasi">Logout</button>
        </div>
      </header>

      <section class="card" id="summaryCard" style="margin-bottom:12px">
        <div class="head">
          <h3>Ringkasan</h3>
          <span class="badge" id="countBadge">0 transaksi</span>
        </div>
        <div class="body">
          <div class="stats">
            <div class="stat">
              <div class="k">Total pemasukan</div>
              <div class="v pos" id="sumIncome">Rp 0</div>
            </div>
            <div class="stat">
              <div class="k">Total pengeluaran</div>
              <div class="v neg" id="sumExpense">Rp 0</div>
            </div>
            <div class="stat">
              <div class="k">Saldo</div>
              <div class="v" id="balance">Rp 0</div>
            </div>
          </div>

          <div class="sp12"></div>

          <div class="row" style="flex-direction:column;gap:10px">
            <div style="min-width:100%">
              <div class="k" style="font-size:12px;color:var(--muted);margin-bottom:6px">Filter akun</div>
              <div class="filters" id="acctFilters"></div>
            </div>
            <div class="row" style="gap:8px;display:grid;grid-template-columns:1fr 1fr">
              <button class="btn ghost" id="manageAccTypesBtn" type="button" title="Tambah / edit jenis akun">Kelola Akun</button>
              <button class="btn ghost" id="manageCatsTopBtn" type="button" title="Tambah / edit kategori">Kelola Kategori</button>
            </div>
          </div>

          <div class="sp12"></div>
          <div class="miniStats" id="acctStats"></div>
        </div>
      </section>

      <div id="addBtnSlot">
        <button class="btn addGreen block" id="openAddTab" type="button" title="Tambah transaksi" aria-label="Tambah transaksi">
          <span class="plus" aria-hidden="true">
            <svg width="18" height="18" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round">
              <path d="M12 5v14" />
              <path d="M5 12h14" />
            </svg>
          </span>
          <span>Tambah</span>
        </button>
      </div>

      <div class="sp14"></div>

      <div class="grid">
        <section class="card">
          <div class="head">
            <h3>Transaksi</h3>
            <span class="badge">Daftar transaksi</span>
          </div>
          <div class="body">
            <div class="txFilters">
              <div class="field">
                <label for="search">Pencarian</label>
                <input id="search" type="text" placeholder="cari kategori/catatan…" />
              </div>
              <div class="field sm">
                <label for="month">Filter bulan</label>
                <input id="month" type="month" />
              </div>
            </div>

            <div class="sp10"></div>
            <div class="hint">Klik tombol <b>Tambah</b> di atas untuk mengisi detail transaksi.</div>
            <div class="sp14"></div>
            <div class="txList" id="txList"></div>
          </div>
        </section>
      </div>
    </div>
  </div>

  <!-- Manage Account Types Modal -->
  <div class="modalMask" id="accTypeMask"></div>
  <div class="modal" id="accTypeModal" aria-hidden="true">
    <div class="modalHead">
      <h3>Kelola Jenis Akun</h3>
      <button class="iconMini" id="closeAccTypeModal" type="button" aria-label="Tutup">✕</button>
    </div>
    <div class="modalBody">
      <div class="muted" style="font-size:12px;margin:0 0 10px">Ubah emoji, nama akun, dan <b>saldo awal</b> (opsional). ID dibuat otomatis.</div>
      <div id="accTypeList"></div>

      <div class="accTypeRow" style="margin-top:6px">
        <div class="accTypeMeta">Tambah</div>
        <input class="emojiIn" id="newAccTypeEmoji" type="text" maxlength="4" placeholder="💳" />
        <input id="newAccTypeName" type="text" placeholder="Contoh: Investasi" />
        <button class="iconMini" id="addAccTypeBtn" type="button" title="Tambah">＋</button>
      </div>
    </div>
    <div class="modalFooter">
      <button class="btn" id="cancelAccTypeBtn" type="button">Batal</button>
      <button class="btn primary" id="saveAccTypeBtn" type="button">Simpan</button>
    </div>
  </div>

  <!-- Manage Categories Modal -->
  <div class="modalMask" id="catMask"></div>
  <div class="modal" id="catModal" aria-hidden="true">
    <div class="modalHead">
      <h3>Kelola Kategori</h3>
      <button class="iconMini" id="closeCatModal" type="button" aria-label="Tutup">✕</button>
    </div>
    <div class="modalBody">
      <div class="muted" style="font-size:12px;margin:0 0 10px">Kategori dipisah: <b>Pengeluaran</b> & <b>Pemasukan</b>. Transfer adalah kategori sistem.</div>

      <div class="filters" id="catTypeTabs" style="padding-bottom:0">
        <button class="filterBtn active" type="button" data-catkind="expense">Pengeluaran</button>
        <button class="filterBtn" type="button" data-catkind="income">Pemasukan</button>
      </div>
      <div class="sp10"></div>

      <div id="catList"></div>

      <div class="accTypeRow" style="margin-top:6px">
        <div class="accTypeMeta">Tambah</div>
        <input class="emojiIn" id="newCatEmoji" type="text" maxlength="4" placeholder="🏷️" />
        <input id="newCatName" type="text" placeholder="Contoh: Kesehatan" />
        <button class="iconMini" id="addCatBtn" type="button" title="Tambah">＋</button>
      </div>
    </div>
    <div class="modalFooter">
      <button class="btn" id="cancelCatBtn" type="button">Batal</button>
      <button class="btn primary" id="saveCatBtn" type="button">Simpan</button>
    </div>
  </div>

  <!-- Add Transaction Tab (Sheet) -->
  <div class="modalMask" id="txMask"></div>
  <div class="modal" id="txModal" aria-hidden="true" style="bottom:12px">
    <div class="modalHead">
      <h3>Tambah transaksi</h3>
      <button class="iconMini" id="closeTxModal" type="button" aria-label="Tutup">✕</button>
    </div>
    <div class="modalBody">
      <div class="muted" style="font-size:12px;margin:0 0 10px">Isi detail transaksi, lalu simpan.</div>

      <div class="txForm">
        <div class="field sm">
          <label for="type">Tipe</label>
          <select id="type">
            <option value="income">Pemasukan</option>
            <option value="expense">Pengeluaran</option>
            <option value="transfer">Transfer</option>
          </select>
        </div>

        <div class="field sm">
          <label for="amount">Nominal</label>
          <input id="amount" type="number" inputmode="numeric" min="0" step="100" placeholder="50000" />
        </div>

        <div class="field sm">
          <label for="date">Tanggal</label>
          <input id="date" type="date" />
        </div>

        <div class="field sm" id="singleAcctField">
          <label for="acctType">Akun</label>
          <select id="acctType"></select>
        </div>

        <div class="field sm hidden" id="transferFromField">
          <label for="transferFrom">Dari akun</label>
          <select id="transferFrom"></select>
        </div>

        <div class="field sm hidden" id="transferToField">
          <label for="transferTo">Ke akun</label>
          <select id="transferTo"></select>
        </div>

        <div class="field col2" id="categoryField">
          <label for="category">Kategori</label>
          <select id="category"></select>
          <div class="hint" style="margin-top:8px">Kelola kategori ada di <b>Ringkasan</b> (bagian atas).</div>
        </div>

        <div class="field col2">
          <label for="note">Catatan</label>
          <input id="note" type="text" placeholder="opsional" />
        </div>
      </div>

      <div class="hint" style="margin-top:12px">Tips: Transfer akan memindahkan saldo antar akun (misal Bank → E-Wallet).</div>
    </div>
    <div class="modalFooter">
      <button class="btn" id="cancelTxBtn" type="button">Batal</button>
      <button class="btn primary" id="addBtn" type="button">Simpan</button>
    </div>
  </div>

  <!-- Reset Confirm Modal -->
  <div class="modalMask" id="resetMask"></div>
  <div class="modal" id="resetModal" aria-hidden="true" style="bottom:12px">
    <div class="modalHead">
      <h3>Konfirmasi Reset</h3>
      <button class="iconMini" id="closeResetModal" type="button" aria-label="Tutup">✕</button>
    </div>
    <div class="modalBody">
      <div style="display:flex;gap:10px;align-items:flex-start">
        <div style="width:42px;height:42px;border-radius:14px;border:1px solid rgba(255,255,255,.14);background:rgba(248,113,113,.12);display:grid;place-items:center;font-size:18px">⚠️</div>
        <div>
          <div style="font-weight:750">Hapus semua transaksi?</div>
          <div class="muted" style="font-size:12px;margin-top:4px;line-height:1.4">
            Tindakan ini akan menghapus <b>seluruh</b> riwayat transaksi dari perangkat ini. Tidak bisa dibatalkan.
          </div>
          <div class="hint" style="margin-top:10px">Saran: tekan <b>Backup CSV</b> dulu kalau ingin menyimpan data.</div>
        </div>
      </div>
    </div>
    <div class="modalFooter">
      <button class="btn" id="cancelResetBtn" type="button">Batal</button>
      <button class="btn danger" id="confirmResetBtn" type="button">Ya, Reset</button>
    </div>
  </div>

  <!-- Transaction Detail Modal -->
  <div class="modalMask" id="txDetailMask"></div>
  <div class="modal" id="txDetailModal" aria-hidden="true" style="bottom:12px">
    <div class="modalHead">
      <h3>Detail transaksi</h3>
      <button class="iconMini" id="closeTxDetail" type="button" aria-label="Tutup">✕</button>
    </div>
    <div class="modalBody">
      <div class="muted" style="font-size:12px;margin:0 0 10px">Klik <b>Edit</b> untuk mengubah, atau <b>Hapus</b> untuk menghapus transaksi.</div>
      <div class="detailGrid" id="txDetailGrid"></div>
      <div class="hint" id="txDetailHint" style="margin-top:12px"></div>
    </div>
    <div class="modalFooter">
      <button class="btn" id="txDetailCloseBtn" type="button">Tutup</button>
      <button class="btn primary" id="txDetailEditBtn" type="button">Edit</button>
    </div>
    <div style="padding:0 4px 6px">
      <button class="btn danger block" id="txDetailDeleteBtn" type="button">Hapus transaksi</button>
    </div>
  </div>

  <div class="toast" id="toast">Tersimpan.</div>

  <script>
    // ===== Keys (local) =====
    const KEY_TX = 'finance_tx_v4';
    const KEY_TYPES = 'finance_account_types_v1';
    const KEY_CATS = 'finance_categories_v2';
    const KEY_PIN = 'finance_pin_v1'; // {salt:"...", hash:"..."}
    const KEY_RECOVERY_PIN = 'finance_recovery_pin_v1'; // {salt:"...", hash:"..."} (PIN pemulihan per user/per perangkat)

    // ===== Helpers =====
    const $ = (id) => document.getElementById(id);

    function toast(msg) {
      const t = $('toast');
      t.textContent = msg;
      t.classList.add('show');
      clearTimeout(window.__toastTimer);
      window.__toastTimer = setTimeout(() => t.classList.remove('show'), 1400);
    }

    function fmt(n) {
      return new Intl.NumberFormat('id-ID', {
        style: 'currency',
        currency: 'IDR',
        maximumFractionDigits: 0
      }).format(Number(n || 0));
    }

    function todayISO() {
      return new Date().toISOString().slice(0, 10);
    }

    function monthOf(d) {
      return String(d || '').slice(0, 7);
    }

    // CSV escaping without regex
    // NOTE: previous error "Invalid or unexpected token" typically happens when a literal newline
    // accidentally appears inside quotes like ' ... <newline> ... '. We use explicit \n/\r.
    function csvEscape(v) {
      const s = String(v ?? '');
      const need = s.includes(',') || s.includes('"') || s.includes('\n') || s.includes('\r');
      const out = s.split('"').join('""');
      return need ? `"${out}"` : out;
    }

    function escapeHtml(s) {
      const str = String(s ?? '');
      return str
        .split('&').join('&amp;')
        .split('<').join('&lt;')
        .split('>').join('&gt;')
        .split('"').join('&quot;')
        .split("'").join('&#39;');
    }

    // slugify without regex
    function slugifyLabel(label) {
      const s = String(label || '').trim().toLowerCase();
      let out = '';
      let prevDash = false;

      for (let i = 0; i < s.length; i++) {
        const ch = s[i];
        const code = ch.charCodeAt(0);
        const isNum = code >= 48 && code <= 57;
        const isAz = code >= 97 && code <= 122;
        if (isNum || isAz) {
          out += ch;
          prevDash = false;
        } else {
          if (!prevDash && out.length > 0) {
            out += '-';
            prevDash = true;
          }
        }
        if (out.length >= 24) break;
      }

      out = out.split(' ').join('');
      while (out.startsWith('-')) out = out.slice(1);
      while (out.endsWith('-')) out = out.slice(0, -1);

      return out || 'item';
    }

    function uniqId(base, existsFn) {
      let id = base;
      let i = 2;
      while (existsFn(id)) id = `${base}-${i++}`;
      return id;
    }

    function loadJson(key, fallback) {
      try {
        const raw = localStorage.getItem(key);
        return raw ? JSON.parse(raw) : fallback;
      } catch {
        return fallback;
      }
    }

    function saveJson(key, value) {
      localStorage.setItem(key, JSON.stringify(value));
    }

    // ===== PIN Auth (local, ringan) =====
    function loadPinRecord(){
      return loadJson(KEY_PIN, null);
    }
    function loadRecoveryRecord(){
      return loadJson(KEY_RECOVERY_PIN, null);
    }

    function b64FromBytes(bytes){
      let bin = '';
      const arr = new Uint8Array(bytes);
      for (let i=0;i<arr.length;i++) bin += String.fromCharCode(arr[i]);
      return btoa(bin);
    }

    async function sha256(str){
      const enc = new TextEncoder();
      const buf = await crypto.subtle.digest('SHA-256', enc.encode(str));
      return b64FromBytes(buf);
    }

    function makeSalt(){
      const arr = new Uint8Array(16);
      crypto.getRandomValues(arr);
      return b64FromBytes(arr);
    }

    async function setPin(pin){
      const p = String(pin || '').trim();
      if (!/^[0-9]{4,12}$/.test(p)) throw new Error('PIN harus 4–12 angka');
      const salt = makeSalt();
      const hash = await sha256(salt + ':' + p);
      saveJson(KEY_PIN, { salt, hash });
    }

    async function setRecoveryPin(pin){
      const p = String(pin || '').trim();
      if (!/^[0-9]{4,12}$/.test(p)) throw new Error('Recovery PIN harus 4–12 angka');
      const salt = makeSalt();
      const hash = await sha256(salt + ':' + p);
      saveJson(KEY_RECOVERY_PIN, { salt, hash });
    }

    async function verifyPin(pin){
      const p = String(pin || '').trim();

      // 1) Coba PIN utama
      const rec = loadPinRecord();
      if (rec && rec.salt && rec.hash) {
        const hash = await sha256(String(rec.salt) + ':' + p);
        if (hash === rec.hash) return { ok:true, via:'pin' };
      }

      // 2) Coba Recovery PIN (per user/per perangkat)
      const r = loadRecoveryRecord();
      if (r && r.salt && r.hash) {
        const rh = await sha256(String(r.salt) + ':' + p);
        if (rh === r.hash) return { ok:true, via:'recovery' };
      }

      return { ok:false, via:'' };
    }

    function clearAllData(){
      localStorage.removeItem(KEY_TX);
      localStorage.removeItem(KEY_TYPES);
      localStorage.removeItem(KEY_CATS);
      localStorage.removeItem(KEY_PIN);
      localStorage.removeItem(KEY_RECOVERY_PIN);
    }

    // ===== State =====
    let tx = loadJson(KEY_TX, []);
    let accountFilter = 'all';

    // ----- Accounts -----
    let accountTypes = loadJson(KEY_TYPES, null);
    if (!Array.isArray(accountTypes) || accountTypes.length === 0) {
      accountTypes = [
        { id: 'cash', label: 'Cash', emoji: '💵', opening: 0 },
        { id: 'bank', label: 'Bank', emoji: '🏦', opening: 0 },
        { id: 'ewallet', label: 'E-Wallet', emoji: '📱', opening: 0 },
      ];
    } else {
      accountTypes = accountTypes
        .filter((x) => x && typeof x.id === 'string' && typeof x.label === 'string')
        .map((x) => ({
          id: x.id,
          label: x.label,
          emoji: (typeof x.emoji === 'string' ? x.emoji : ''),
          opening: Number(x.opening || 0)
        }))
        .slice(0, 12);

      if (accountTypes.length === 0) {
        accountTypes = [{ id: 'cash', label: 'Cash', emoji: '💵', opening: 0 }];
      }
    }

    // ----- Categories (income/expense) -----
    function inferCatKind(label, id) {
      const s = String(label || '').trim().toLowerCase();
      const sid = String(id || '').trim().toLowerCase();

      if (sid === 'transfer' || s === 'transfer' || s.includes('transfer')) return 'transfer';

      const incomeHints = ['gaji','salary','freelance','bonus','hadiah','gift','dividen','penjualan','jualan','refund','reimburse','komisi'];
      for (const k of incomeHints) {
        if (s.includes(k)) return 'income';
      }

      return 'expense';
    }

    let categories = loadJson(KEY_CATS, null);
    if (!Array.isArray(categories) || categories.length === 0) {
      categories = [
        { id: 'gaji', label: 'Gaji', emoji: '💼', kind: 'income' },
        { id: 'freelance', label: 'Freelance', emoji: '🧑‍💻', kind: 'income' },
        { id: 'hadiah', label: 'Hadiah', emoji: '🎁', kind: 'income' },

        { id: 'makan', label: 'Makan', emoji: '🍜', kind: 'expense' },
        { id: 'bensin', label: 'Bensin', emoji: '⛽', kind: 'expense' },
        { id: 'belanja', label: 'Belanja', emoji: '🛒', kind: 'expense' },
        { id: 'hiburan', label: 'Hiburan', emoji: '🎮', kind: 'expense' },

        { id: 'transfer', label: 'Transfer', emoji: '🔁', kind: 'transfer' },
      ];
    } else {
      categories = categories
        .filter((x) => x && typeof x.id === 'string' && typeof x.label === 'string')
        .map((x) => ({
          id: x.id,
          label: x.label,
          emoji: (typeof x.emoji === 'string' ? x.emoji : ''),
          kind: (x.kind === 'income' || x.kind === 'expense' || x.kind === 'transfer') ? x.kind : inferCatKind(x.label, x.id)
        }))
        .slice(0, 80);

      if (categories.length === 0) {
        categories = [{ id: 'makan', label: 'Makan', emoji: '🍜', kind: 'expense' }];
      }
    }

    function saveTx(){ saveJson(KEY_TX, tx); }
    function saveTypes(){ saveJson(KEY_TYPES, accountTypes); }
    function saveCats(){ saveJson(KEY_CATS, categories); }

    function ensureTransferCategory() {
      const hit = categories.find((c) =>
        c.kind === 'transfer' ||
        String(c.id || '').toLowerCase() === 'transfer' ||
        String(c.label || '').toLowerCase() === 'transfer'
      );

      if (hit) {
        hit.kind = 'transfer';
        if (!hit.label) hit.label = 'Transfer';
        if (!hit.emoji) hit.emoji = '🔁';
        if (!hit.id) hit.id = 'transfer';
        saveCats();
        return hit.id;
      }

      const id = uniqId('transfer', (x) => categories.some((c) => c.id === x));
      categories.push({ id, label: 'Transfer', emoji: '🔁', kind: 'transfer' });
      saveCats();
      return id;
    }

    ensureTransferCategory();

    function catKindOf(id) {
      const c = categories.find((x) => x.id === id);
      return c?.kind || inferCatKind(c?.label, c?.id) || 'expense';
    }

    function acctLabel(id) {
      const a = accountTypes.find((x) => x.id === id);
      if (!a) return id || 'Akun';
      return `${a.emoji ? a.emoji + ' ' : ''}${a.label}`.trim();
    }

    function acctLabelPlain(id){
      const a = accountTypes.find((x) => x.id === id);
      return a ? a.label : (id || 'Akun');
    }

    function catLabel(id) {
      const c = categories.find((x) => x.id === id);
      if (!c) return id || 'Kategori';
      return `${c.emoji ? c.emoji + ' ' : ''}${c.label}`.trim();
    }

    function catLabelPlain(id){
      const c = categories.find((x) => x.id === id);
      return c ? c.label : (id || 'Kategori');
    }

    // Backward-compatible API (old tests call ensureCategory('Transfer'))
    function ensureCategory(label, kind) {
      const v = String(label || '').trim();
      if (!v) {
        const any = categories.find((c) => c.kind === (kind || 'expense'));
        return any?.id || categories[0]?.id;
      }

      const lower = v.toLowerCase();
      if (lower === 'transfer' || lower.includes('transfer')) return ensureTransferCategory();

      const desiredKind = (kind === 'income' || kind === 'expense') ? kind : inferCatKind(v, v);

      const hit = categories.find((c) => c.kind === desiredKind && String(c.label || '').toLowerCase() === lower);
      if (hit) return hit.id;

      const base = uniqId(slugifyLabel(v), (id) => categories.some((c) => c.id === id));
      categories.push({ id: base, label: v, emoji: '🏷️', kind: desiredKind });
      saveCats();
      return base;
    }

    // ===== Normalize / Migrate tx =====
    function normalizeTx(){
      let changed = false;
      const transferId = ensureTransferCategory();

      for (const t of tx) {
        // ensure schema basics
        if (!t.id) {
          t.id = (crypto.randomUUID ? crypto.randomUUID() : String(Date.now() + Math.random()));
          changed = true;
        }
        if (!t.date) {
          t.date = todayISO();
          changed = true;
        }

        // default accountType
        if (!t.accountType && t.type !== 'transfer') {
          t.accountType = accountTypes[0]?.id || 'cash';
          changed = true;
        }

        // ensure from/to for transfer
        if (t.type === 'transfer') {
          if (!t.fromAccountType) t.fromAccountType = t.accountType || (accountTypes[0]?.id || 'cash');
          if (!t.toAccountType) t.toAccountType = accountTypes[0]?.id || 'cash';
          t.accountType = t.fromAccountType;

          if (t.categoryId !== transferId) {
            t.categoryId = transferId;
            changed = true;
          }

          continue;
        }

        // categoryId migration
        if (!t.categoryId) {
          const legacy = String(t.category || '').trim();
          if (legacy) {
            const wantKind = (t.type === 'income') ? 'income' : 'expense';
            const hit = categories.find((c) => c.kind === wantKind && String(c.label || '').toLowerCase() === legacy.toLowerCase());
            if (hit) t.categoryId = hit.id;
            else t.categoryId = ensureCategory(legacy, wantKind);
            changed = true;
          }
        }

        // if category exists but kind mismatched, attempt to map by label
        if (t.categoryId) {
          const wantKind = (t.type === 'income') ? 'income' : 'expense';
          const k = catKindOf(t.categoryId);
          if (k !== wantKind) {
            const label = catLabelPlain(t.categoryId);
            const mapped = categories.find((c) => c.kind === wantKind && String(c.label || '').toLowerCase() === String(label || '').toLowerCase());
            t.categoryId = mapped ? mapped.id : ensureCategory(label || 'Kategori', wantKind);
            changed = true;
          }
        }
      }

      if (changed) {
        saveCats();
        saveTx();
      }
    }

    normalizeTx();

    // ===== Filtering =====
    function monthMatch(t) {
      const m = $('month').value;
      return !m || monthOf(t.date) === m;
    }

    function accountMatch(t) {
      if (accountFilter === 'all') return true;

      if (t.type === 'transfer') {
        const fromId = t.fromAccountType || t.accountType || (accountTypes[0]?.id || 'cash');
        const toId = t.toAccountType || (accountTypes[0]?.id || 'cash');
        return fromId === accountFilter || toId === accountFilter;
      }

      const tid = (t.accountType || accountTypes[0]?.id || 'cash');
      return tid === accountFilter;
    }

    function getMonthBase() {
      return tx.filter((t) => monthMatch(t));
    }

    function getBaseForTotals() {
      return getMonthBase().filter((t) => accountMatch(t));
    }

    function getListFiltered() {
      const q = String(($('search').value || '')).trim().toLowerCase();
      return getBaseForTotals()
        .filter((t) => {
          if (!q) return true;
          const cat = catLabel(t.categoryId || '');
          const acct = acctLabel(t.accountType || '');
          const from = acctLabel(t.fromAccountType || '');
          const to = acctLabel(t.toAccountType || '');
          const note = String(t.note || '');
          return (`${cat} ${acct} ${from} ${to} ${note}`.toLowerCase().includes(q));
        })
        .sort((a, b) => String(b.date || '').localeCompare(String(a.date || '')));
    }

    // ===== UI rendering =====
    function renderAccountTypeSelect() {
      const fill = (selId) => {
        const sel = $(selId);
        if (!sel) return;
        const current = sel.value;
        sel.innerHTML = '';
        for (const t of accountTypes) {
          const opt = document.createElement('option');
          opt.value = t.id;
          opt.textContent = `${t.emoji ? t.emoji + ' ' : ''}${t.label}`.trim();
          sel.appendChild(opt);
        }
        if (accountTypes.some((t) => t.id === current)) sel.value = current;
        else sel.value = accountTypes[0]?.id || 'cash';
      };

      fill('acctType');
      fill('transferFrom');
      fill('transferTo');
    }

    let lastExpenseCatId = '';
    let lastIncomeCatId = '';

    function renderCategorySelect() {
      const sel = $('category');
      if (!sel) return;

      const type = $('type')?.value || 'income';

      // transfer: kategori sistem, disembunyikan
      if (type === 'transfer') {
        const tid = ensureTransferCategory();
        sel.innerHTML = '';
        const opt = document.createElement('option');
        opt.value = tid;
        opt.textContent = catLabel(tid);
        sel.appendChild(opt);
        sel.value = tid;
        return;
      }

      const wantKind = (type === 'income') ? 'income' : 'expense';
      const current = sel.value;
      sel.innerHTML = '';

      const ph = document.createElement('option');
      ph.value = '';
      ph.textContent = 'Pilih kategori…';
      sel.appendChild(ph);

      const list = categories
        .filter((c) => c.kind === wantKind)
        .slice()
        .sort((a,b) => String(a.label||'').localeCompare(String(b.label||'')));

      for (const c of list) {
        const opt = document.createElement('option');
        opt.value = c.id;
        opt.textContent = `${c.emoji ? c.emoji + ' ' : ''}${c.label}`.trim();
        sel.appendChild(opt);
      }

      if (list.some((c) => c.id === current)) {
        sel.value = current;
      } else {
        const last = (wantKind === 'income') ? lastIncomeCatId : lastExpenseCatId;
        sel.value = (last && list.some((c)=>c.id===last)) ? last : '';
      }
    }

    function renderAccountTypeFilters() {
      const wrap = $('acctFilters');
      wrap.innerHTML = '';

      const mkBtn = (label, id) => {
        const b = document.createElement('button');
        b.type = 'button';
        b.className = 'filterBtn' + ((accountFilter === id) ? ' active' : '');
        b.dataset.acct = id;
        b.textContent = label;
        b.addEventListener('click', () => {
          accountFilter = id;
          render();
        });
        return b;
      };

      wrap.appendChild(mkBtn('Semua', 'all'));
      for (const t of accountTypes) wrap.appendChild(mkBtn(`${t.emoji ? t.emoji + ' ' : ''}${t.label}`.trim(), t.id));
    }

    function renderAccountTypeStats(monthBase) {
      const bal = {};
      for (const t of accountTypes) bal[t.id] = Number(t.opening || 0);

      for (const it of monthBase) {
        if (it.type === 'transfer') {
          const fromId = it.fromAccountType || it.accountType || (accountTypes[0]?.id);
          const toId = it.toAccountType || (accountTypes[0]?.id);
          if (fromId) bal[fromId] = (bal[fromId] || 0) - (it.amount || 0);
          if (toId) bal[toId] = (bal[toId] || 0) + (it.amount || 0);
          continue;
        }

        const tid = (it.accountType || accountTypes[0]?.id);
        if (!tid) continue;
        bal[tid] = (bal[tid] || 0) + ((it.type === 'income') ? it.amount : -it.amount);
      }

      const box = $('acctStats');
      box.innerHTML = '';
      for (const t of accountTypes) {
        const card = document.createElement('div');
        card.className = 'miniStat';
        card.innerHTML = `
          <div class="k">${escapeHtml(`${t.emoji ? t.emoji + ' ' : ''}${t.label}`.trim())}</div>
          <div class="v">${fmt(bal[t.id] || 0)}</div>
        `;
        box.appendChild(card);
      }
    }

    function typeText(t) {
      return (t === 'income' ? 'Pemasukan' : (t === 'expense' ? 'Pengeluaran' : 'Transfer'));
    }

    // ===== Main render =====
    function render() {
      renderAccountTypeSelect();
      renderCategorySelect();

      const monthBase = getMonthBase();
      const baseForTotals = getBaseForTotals();
      const list = getListFiltered();

      let inc = 0, exp = 0;
      for (const t of baseForTotals) {
        if (t.type === 'transfer') continue;
        if (t.type === 'income') inc += Number(t.amount || 0);
        else exp += Number(t.amount || 0);
      }

      $('sumIncome').textContent = fmt(inc);
      $('sumExpense').textContent = fmt(exp);

      const openingSum = (accountFilter === 'all')
        ? accountTypes.reduce((s, a) => s + Number(a.opening || 0), 0)
        : Number(accountTypes.find((a) => a.id === accountFilter)?.opening || 0);

      $('balance').textContent = fmt(openingSum + (inc - exp));
      $('countBadge').textContent = `${list.length} transaksi`;

      renderAccountTypeFilters();
      renderAccountTypeStats(monthBase);

      const box = $('txList');
      box.innerHTML = '';

      if (list.length === 0) {
        box.innerHTML = `<div class="muted" style="font-size:13px">Belum ada transaksi untuk filter ini.</div>`;
        return;
      }

      const prettyDate = (iso) => {
        try {
          return new Intl.DateTimeFormat('id-ID', { day: '2-digit', month: 'short', year: 'numeric' }).format(new Date(iso));
        } catch {
          return iso;
        }
      };

      const groups = new Map();
      for (const t of list) {
        const d = t.date || '';
        if (!groups.has(d)) groups.set(d, []);
        groups.get(d).push(t);
      }

      const dates = Array.from(groups.keys()).sort((a, b) => String(b || '').localeCompare(String(a || '')));

      for (const d of dates) {
        const dayWrap = document.createElement('div');
        dayWrap.className = 'txDay';

        const items = groups.get(d) || [];
        const head = document.createElement('div');
        head.className = 'txDayHead';
        head.innerHTML = `<div class="d">${escapeHtml(prettyDate(d))}</div><div class="c">${items.length} item</div>`;
        dayWrap.appendChild(head);

        for (const t of items) {
          const isTransfer = t.type === 'transfer';
          const isExp = t.type === 'expense';
          const label = isTransfer ? 'Transfer' : (isExp ? 'Pengeluaran' : 'Pemasukan');

          const fromId = t.fromAccountType || t.accountType || '';
          const toId = t.toAccountType || '';
          const acctText = isTransfer ? `${acctLabel(fromId)} → ${acctLabel(toId)}` : acctLabel(t.accountType || '');
          const catText = catLabel(t.categoryId || '') || (t.category || '');

          const item = document.createElement('div');
          item.className = 'txItem';
          item.setAttribute('role','button');
          item.setAttribute('tabindex','0');
          item.dataset.id = t.id;

          const amt = isTransfer ? Number(t.amount || 0) : (isExp ? -Number(t.amount || 0) : Number(t.amount || 0));
          const amtCls = isTransfer ? 'muted' : (isExp ? 'neg' : 'pos');

          item.innerHTML = `
            <div class="txMain">
              <div class="txTitle">
                <span class="chip"><span class="dot ${isTransfer ? 'trf' : (isExp ? 'exp' : '')}"></span>${label}</span>
                <span style="font-weight:750">${escapeHtml(catText || (isTransfer ? 'Transfer' : ''))}</span>
              </div>
              <div class="txMeta">
                <span class="chip">${escapeHtml(acctText)}</span>
              </div>
              ${t.note ? `<div class="txNote">${escapeHtml(t.note)}</div>` : ``}
            </div>
            <div class="txRight">
              <div class="txAmt ${amtCls}">${fmt(amt)}</div>
              <div class="txChevron" aria-hidden="true">›</div>
            </div>
          `;

          item.addEventListener('click', () => openTxDetail(t.id));
          item.addEventListener('keydown', (e) => {
            if (e.key === 'Enter' || e.key === ' ') {
              e.preventDefault();
              openTxDetail(t.id);
            }
          });

          dayWrap.appendChild(item);
        }

        box.appendChild(dayWrap);
      }
    }

    // ===== Actions =====
    let editingTxId = null;
    let detailTxId = null;

    function clearEditMode(){
      editingTxId = null;
      try{ $('txModal').querySelector('h3').textContent = 'Tambah transaksi'; }catch{}
      try{ $('addBtn').textContent = 'Simpan'; }catch{}
    }

    function resetTxForm(){
      $('type').value = 'income';
      $('amount').value = '';
      $('note').value = '';
      $('date').value = todayISO();
      $('acctType').value = accountTypes[0]?.id || 'cash';
      $('transferFrom').value = accountTypes[0]?.id || 'cash';
      $('transferTo').value = (accountTypes[1]?.id || accountTypes[0]?.id || 'cash');
      $('type').dispatchEvent(new Event('change'));
    }

    function upsertTx(obj){
      if (!editingTxId) {
        tx.push(obj);
        return;
      }
      const i = tx.findIndex((x) => x.id === editingTxId);
      if (i === -1) tx.push(obj);
      else tx[i] = { ...tx[i], ...obj, id: editingTxId };
    }

    function deleteTxById(id){
      tx = tx.filter((x) => x.id !== id);
      saveTx();
      render();
      toast('Transaksi dihapus');
    }

    function openTxDetail(id){
      const t = tx.find((x) => x.id === id);
      if (!t) return;
      detailTxId = id;

      const isTransfer = t.type === 'transfer';
      const isExp = t.type === 'expense';
      const label = isTransfer ? 'Transfer' : (isExp ? 'Pengeluaran' : 'Pemasukan');

      const pretty = (iso) => {
        try {
          return new Intl.DateTimeFormat('id-ID', { day: '2-digit', month: 'long', year: 'numeric' }).format(new Date(iso));
        } catch {
          return iso;
        }
      };

      const amt = isTransfer ? Number(t.amount || 0) : (isExp ? -Number(t.amount || 0) : Number(t.amount || 0));

      const rows = [
        { k:'Tipe', v: label },
        { k:'Tanggal', v: pretty(t.date || '') },
        { k:'Nominal', v: fmt(amt) },
        { k:'Kategori', v: catLabel(t.categoryId || '') },
      ];

      if (isTransfer) {
        const fromId = t.fromAccountType || t.accountType || (accountTypes[0]?.id || 'cash');
        const toId = t.toAccountType || (accountTypes[0]?.id || 'cash');
        rows.push({ k:'Dari akun', v: acctLabel(fromId) });
        rows.push({ k:'Ke akun', v: acctLabel(toId) });
      } else {
        rows.push({ k:'Akun', v: acctLabel(t.accountType || (accountTypes[0]?.id || 'cash')) });
      }

      if (t.note) rows.push({ k:'Catatan', v: t.note });

      $('txDetailGrid').innerHTML = rows.map(r => `
        <div class="detailRow">
          <div class="k">${escapeHtml(r.k)}</div>
          <div class="v">${escapeHtml(r.v)}</div>
        </div>
      `).join('');

      $('txDetailHint').textContent = `ID: ${t.id}`;
      $('txDetailDeleteBtn').dataset.stage = '';
      $('txDetailDeleteBtn').textContent = 'Hapus transaksi';

      $('txDetailMask').classList.add('show');
      $('txDetailModal').classList.add('show');
      $('txDetailModal').setAttribute('aria-hidden', 'false');
    }

    function closeTxDetail(){
      $('txDetailMask').classList.remove('show');
      $('txDetailModal').classList.remove('show');
      $('txDetailModal').setAttribute('aria-hidden', 'true');
      detailTxId = null;
    }

    function startEditTx(id){
      const t = tx.find((x) => x.id === id);
      if (!t) return;
      editingTxId = id;

      $('txModal').querySelector('h3').textContent = 'Edit transaksi';
      $('addBtn').textContent = 'Simpan perubahan';

      $('type').value = t.type || 'income';
      $('type').dispatchEvent(new Event('change'));

      $('amount').value = Number(t.amount || 0);
      $('date').value = t.date || todayISO();
      $('note').value = t.note || '';

      if (t.type === 'transfer') {
        $('transferFrom').value = t.fromAccountType || t.accountType || (accountTypes[0]?.id || 'cash');
        $('transferTo').value = t.toAccountType || (accountTypes[0]?.id || 'cash');
      } else {
        $('acctType').value = t.accountType || (accountTypes[0]?.id || 'cash');
        $('category').value = t.categoryId || '';
      }

      openTxModal();
    }

    function addTx() {
      const type = $('type').value;
      const amount = Number($('amount').value);
      const date = $('date').value;
      const note = String(($('note').value || '')).trim();
      const categoryIdInput = String(($('category').value || '')).trim();

      if (!date) return toast('Tanggal wajib diisi');
      if (!amount || amount <= 0) return toast('Nominal harus > 0');

      const id = editingTxId || (crypto.randomUUID ? crypto.randomUUID() : String(Date.now() + Math.random()));

      if (type === 'transfer') {
        const fromAccountType = $('transferFrom').value || accountTypes[0]?.id || 'cash';
        const toAccountType = $('transferTo').value || accountTypes[0]?.id || 'cash';
        if (fromAccountType === toAccountType) return toast('Akun asal & tujuan harus beda');

        const transferCatId = ensureTransferCategory();

        upsertTx({
          id,
          type: 'transfer',
          amount,
          date,
          categoryId: transferCatId,
          fromAccountType,
          toAccountType,
          accountType: fromAccountType,
          note,
        });

        saveTx();
        render();
        closeTxModal();
        toast(editingTxId ? 'Perubahan disimpan' : 'Transfer dicatat');
        clearEditMode();
        resetTxForm();
        return;
      }

      const accountType = $('acctType').value || accountTypes[0]?.id || 'cash';
      const categoryId = categoryIdInput;
      if (!categoryId) return toast('Kategori wajib diisi');

      const wantKind = (type === 'income') ? 'income' : 'expense';
      if (catKindOf(categoryId) !== wantKind) {
        toast(`Kategori harus ${wantKind === 'income' ? 'pemasukan' : 'pengeluaran'}`);
        renderCategorySelect();
        return;
      }

      if (wantKind === 'income') lastIncomeCatId = categoryId;
      else lastExpenseCatId = categoryId;

      upsertTx({
        id,
        type,
        amount,
        date,
        categoryId,
        accountType,
        fromAccountType: null,
        toAccountType: null,
        note,
      });

      saveTx();
      render();
      closeTxModal();
      toast(editingTxId ? 'Perubahan disimpan' : 'Transaksi ditambahkan');
      clearEditMode();
      resetTxForm();
    }

    function seed() {
      const d = (daysAgo) => {
        const dt = new Date();
        dt.setDate(dt.getDate() - daysAgo);
        return dt.toISOString().slice(0, 10);
      };

      const firstAcct = accountTypes[0]?.id || 'cash';
      const pickAcct = (id) => accountTypes.some((t) => t.id === id) ? id : firstAcct;

      const pickCat = (label, kind) => {
        const lower = String(label || '').toLowerCase();
        const hit = categories.find((c) => c.kind === kind && String(c.label || '').toLowerCase() === lower);
        return hit ? hit.id : ensureCategory(label, kind);
      };

      const transferId = ensureTransferCategory();

      tx = [
        { id: '1', type: 'income', amount: 5500000, date: d(8), categoryId: pickCat('Gaji','income'), accountType: pickAcct('bank'), note: 'Payroll' },
        { id: '2', type: 'expense', amount: 65000, date: d(7), categoryId: pickCat('Makan','expense'), accountType: pickAcct('ewallet'), note: 'Sarapan' },
        { id: '3', type: 'expense', amount: 120000, date: d(6), categoryId: pickCat('Bensin','expense'), accountType: pickAcct('cash'), note: 'Isi bensin' },
        { id: '4', type: 'expense', amount: 250000, date: d(5), categoryId: pickCat('Belanja','expense'), accountType: pickAcct('bank'), note: 'Kebutuhan rumah' },
        { id: '5', type: 'income', amount: 300000, date: d(3), categoryId: pickCat('Freelance','income'), accountType: pickAcct('bank'), note: 'Project kecil' },
        { id: '6', type: 'expense', amount: 89000, date: d(2), categoryId: pickCat('Hiburan','expense'), accountType: pickAcct('ewallet'), note: 'Nonton' },
        { id: '7', type: 'transfer', amount: 250000, date: d(1), categoryId: transferId, fromAccountType: pickAcct('bank'), toAccountType: pickAcct('ewallet'), accountType: pickAcct('bank'), note: 'Top up e-wallet' },
      ];

      $('month').value = monthOf(todayISO());
      $('search').value = '';
      saveTx();
      render();
      toast('Contoh data terisi');
    }

    function openResetConfirm(){
      if (!Array.isArray(tx) || tx.length === 0) {
        toast('Tidak ada data untuk direset');
        return;
      }
      closeTxModal();
      closeTxDetail();
      closeAccTypeModal();
      closeCatModal();

      $('resetMask').classList.add('show');
      $('resetModal').classList.add('show');
      $('resetModal').setAttribute('aria-hidden','false');
    }

    function closeResetConfirm(){
      $('resetMask').classList.remove('show');
      $('resetModal').classList.remove('show');
      $('resetModal').setAttribute('aria-hidden','true');
    }

    function resetAll() {
      tx = [];
      $('search').value = '';
      $('month').value = '';
      saveTx();
      render();
      toast('Data direset');
    }

    function exportCSV() {
      if (!Array.isArray(tx) || tx.length === 0) {
        toast('Tidak ada data untuk diekspor');
        return;
      }

      const rows = [];
      rows.push([
        'ID','Tanggal','Bulan','Tipe','Jumlah',
        'Kategori','KategoriID','KategoriKind',
        'Akun','AkunID',
        'Dari Akun','DariAkunID',
        'Ke Akun','KeAkunID',
        'Catatan'
      ]);

      const data = [...tx].sort((a,b) => String(a.date || '').localeCompare(String(b.date || '')));

      for (const t of data) {
        const isTransfer = t.type === 'transfer';
        const date = t.date || '';
        const month = monthOf(date);
        const jumlah = Number(t.amount || 0);

        const cat = catLabelPlain(t.categoryId || '') || '';
        const catKind = catKindOf(t.categoryId || '');
        const akun = (!isTransfer) ? acctLabelPlain(t.accountType || '') : '';
        const dari = isTransfer ? acctLabelPlain(t.fromAccountType || t.accountType || '') : '';
        const ke = isTransfer ? acctLabelPlain(t.toAccountType || '') : '';

        rows.push([
          t.id || '',
          date,
          month,
          typeText(t.type),
          jumlah,
          cat,
          (t.categoryId || ''),
          catKind,
          akun,
          (!isTransfer ? (t.accountType || '') : ''),
          dari,
          (isTransfer ? (t.fromAccountType || t.accountType || '') : ''),
          ke,
          (isTransfer ? (t.toAccountType || '') : ''),
          t.note || '',
        ]);
      }

      const NEWLINE = '\r\n';
      const csv = '\uFEFF' + rows.map(r => r.map(csvEscape).join(',')).join(NEWLINE);
      const blob = new Blob([csv], { type: 'text/csv;charset=utf-8;' });

      const a = document.createElement('a');
      const ts = todayISO();
      a.href = URL.createObjectURL(blob);
      a.download = `catatan-keuangan_${ts}.csv`;
      document.body.appendChild(a);
      a.click();
      a.remove();

      setTimeout(() => URL.revokeObjectURL(a.href), 1000);
      toast('Backup CSV terunduh');
    }

    // ===== Manage Account Types Modal =====
    function openAccTypeModal() {
      $('accTypeMask').classList.add('show');
      $('accTypeModal').classList.add('show');
      $('accTypeModal').setAttribute('aria-hidden', 'false');
      renderAccTypeEditor();
    }

    function closeAccTypeModal() {
      $('accTypeMask').classList.remove('show');
      $('accTypeModal').classList.remove('show');
      $('accTypeModal').setAttribute('aria-hidden', 'true');
      $('newAccTypeName').value = '';
      $('newAccTypeEmoji').value = '';
    }

    function renderAccTypeEditor() {
      const list = $('accTypeList');
      list.innerHTML = '';

      for (const t of accountTypes) {
        const row = document.createElement('div');
        row.className = 'accTypeRow';
        row.innerHTML = `
          <div class="accTypeMeta">ID: ${escapeHtml(t.id)}</div>
          <input class="emojiIn" type="text" maxlength="4" value="${escapeHtml(t.emoji || '')}" data-id-emoji="${escapeHtml(t.id)}" placeholder="💳" />
          <input type="text" value="${escapeHtml(t.label)}" data-id-label="${escapeHtml(t.id)}" />
          <input class="num" type="number" inputmode="numeric" min="0" step="100" value="${Number(t.opening || 0)}" data-id-open="${escapeHtml(t.id)}" placeholder="Saldo awal" />
          <button class="iconMini" type="button" data-del="${escapeHtml(t.id)}" title="Hapus">🗑</button>
        `;
        list.appendChild(row);
      }

      list.querySelectorAll('button[data-del]').forEach((btn) => {
        btn.addEventListener('click', () => {
          const id = btn.getAttribute('data-del');
          if (accountTypes.length <= 1) return toast('Minimal 1 jenis akun');

          if (btn.dataset.stage !== 'confirm') {
            list.querySelectorAll('button[data-del]').forEach((b) => {
              b.dataset.stage = '';
              b.textContent = '🗑';
            });

            btn.dataset.stage = 'confirm';
            btn.textContent = 'Hapus?';
            toast('Klik sekali lagi untuk hapus');

            clearTimeout(window.__delTypeTimer);
            window.__delTypeTimer = setTimeout(() => {
              btn.dataset.stage = '';
              btn.textContent = '🗑';
            }, 1400);
            return;
          }

          const fallback = accountTypes.find((x) => x.id !== id)?.id;
          if (!fallback) return;

          const removed = accountTypes.find((x) => x.id === id);
          const removedOpening = Number(removed?.opening || 0);

          accountTypes = accountTypes.map((x) => {
            if (x.id !== fallback) return x;
            return { ...x, opening: Number(x.opening || 0) + removedOpening };
          });

          tx = tx.map((t) => {
            if (t.type === 'transfer') {
              const from = (t.fromAccountType || fallback) === id ? fallback : (t.fromAccountType || fallback);
              const to = (t.toAccountType || fallback) === id ? fallback : (t.toAccountType || fallback);
              const acct = (t.accountType || fallback) === id ? fallback : (t.accountType || fallback);
              return { ...t, fromAccountType: from, toAccountType: to, accountType: acct };
            }

            const tid = (t.accountType || fallback);
            return (tid === id) ? { ...t, accountType: fallback } : t;
          });

          accountTypes = accountTypes.filter((x) => x.id !== id);
          if (accountFilter === id) accountFilter = 'all';

          saveTypes();
          saveTx();
          renderAccTypeEditor();
          render();
          toast('Jenis akun dihapus');
        });
      });
    }

    function addAccountType() {
      const name = String(($('newAccTypeName').value || '')).trim();
      if (!name) return toast('Nama jenis akun kosong');

      const base = slugifyLabel(name);
      const id = uniqId(base, (x) => accountTypes.some((t) => t.id === x));
      const emoji = String(($('newAccTypeEmoji').value || '')).trim() || '💳';

      accountTypes.push({ id, label: name, emoji, opening: 0 });
      $('newAccTypeName').value = '';
      $('newAccTypeEmoji').value = '';
      saveTypes();
      renderAccTypeEditor();
      render();
      toast('Jenis akun ditambah');
    }

    function saveAccountTypesFromEditor() {
      const emojiInputs = Array.from($('accTypeList').querySelectorAll('input[data-id-emoji]'));
      const labelInputs = Array.from($('accTypeList').querySelectorAll('input[data-id-label]'));
      const openInputs = Array.from($('accTypeList').querySelectorAll('input[data-id-open]'));

      const next = accountTypes.map((t) => ({ ...t, emoji: (typeof t.emoji === 'string' ? t.emoji : ''), opening: Number(t.opening || 0) }));

      for (const inp of emojiInputs) {
        const id = inp.getAttribute('data-id-emoji');
        const v = String((inp.value || '')).trim();
        const item = next.find((x) => x.id === id);
        if (!item) continue;
        item.emoji = v;
      }

      for (const inp of labelInputs) {
        const id = inp.getAttribute('data-id-label');
        const v = String((inp.value || '')).trim();
        const item = next.find((x) => x.id === id);
        if (!item) continue;
        item.label = v || item.label;
      }

      for (const inp of openInputs) {
        const id = inp.getAttribute('data-id-open');
        const n = Number(inp.value);
        const item = next.find((x) => x.id === id);
        if (!item) continue;
        item.opening = Number.isFinite(n) ? Math.max(0, n) : 0;
      }

      accountTypes = next;
      saveTypes();
      closeAccTypeModal();
      render();
      toast('Tersimpan');
    }

    // ===== Manage Categories Modal (split) =====
    let catViewKind = 'expense';

    function syncCatTabs(){
      const tabs = $('catTypeTabs');
      if (!tabs) return;
      tabs.querySelectorAll('button[data-catkind]').forEach((b) => {
        b.classList.toggle('active', (b.getAttribute('data-catkind') || '') === catViewKind);
      });
    }

    function openCatModal() {
      $('catMask').classList.add('show');
      $('catModal').classList.add('show');
      $('catModal').setAttribute('aria-hidden', 'false');

      const tabs = $('catTypeTabs');
      if (tabs && !tabs.dataset.bound) {
        tabs.dataset.bound = '1';
        tabs.querySelectorAll('button[data-catkind]').forEach((b) => {
          b.addEventListener('click', () => {
            catViewKind = b.getAttribute('data-catkind') || 'expense';
            syncCatTabs();
            renderCatEditor();
          });
        });
      }

      syncCatTabs();
      renderCatEditor();
    }

    function closeCatModal() {
      $('catMask').classList.remove('show');
      $('catModal').classList.remove('show');
      $('catModal').setAttribute('aria-hidden', 'true');
      $('newCatName').value = '';
      $('newCatEmoji').value = '';
    }

    function renderCatEditor() {
      syncCatTabs();
      const list = $('catList');
      list.innerHTML = '';

      const shown = categories
        .filter((c) => c.kind === catViewKind)
        .slice()
        .sort((a,b) => String(a.label||'').localeCompare(String(b.label||'')));

      for (const c of shown) {
        const row = document.createElement('div');
        row.className = 'accTypeRow';
        row.innerHTML = `
          <div class="accTypeMeta">ID: ${escapeHtml(c.id)}</div>
          <input class="emojiIn" type="text" maxlength="4" value="${escapeHtml(c.emoji || '')}" data-id-emoji="${escapeHtml(c.id)}" placeholder="🏷️" />
          <input type="text" value="${escapeHtml(c.label)}" data-id="${escapeHtml(c.id)}" />
          <button class="iconMini" type="button" data-del="${escapeHtml(c.id)}" title="Hapus">🗑</button>
        `;
        list.appendChild(row);
      }

      // transfer: sistem
      const transferId = ensureTransferCategory();
      const transfer = categories.find((c)=>c.id===transferId);
      if (transfer) {
        const sys = document.createElement('div');
        sys.className = 'accTypeRow';
        sys.style.opacity = '0.78';
        sys.innerHTML = `
          <div class="accTypeMeta">Sistem (tidak bisa dihapus)</div>
          <input class="emojiIn" type="text" maxlength="4" value="${escapeHtml(transfer.emoji || '🔁')}" disabled />
          <input type="text" value="${escapeHtml(transfer.label || 'Transfer')}" disabled />
          <button class="iconMini" type="button" disabled title="Sistem">🔒</button>
        `;
        list.appendChild(sys);
      }

      list.querySelectorAll('button[data-del]').forEach((btn) => {
        btn.addEventListener('click', () => {
          const id = btn.getAttribute('data-del');
          const item = categories.find((c)=>c.id===id);
          if (!item) return;
          if (item.kind === 'transfer') return toast('Kategori Transfer adalah sistem');

          const sameKindCount = categories.filter((c)=>c.kind===item.kind).length;
          if (sameKindCount <= 1) return toast(`Minimal 1 kategori ${item.kind === 'income' ? 'pemasukan' : 'pengeluaran'}`);

          if (btn.dataset.stage !== 'confirm') {
            list.querySelectorAll('button[data-del]').forEach((b) => {
              b.dataset.stage = '';
              b.textContent = '🗑';
            });

            btn.dataset.stage = 'confirm';
            btn.textContent = 'Hapus?';
            toast('Klik sekali lagi untuk hapus');

            clearTimeout(window.__delCatTimer);
            window.__delCatTimer = setTimeout(() => {
              btn.dataset.stage = '';
              btn.textContent = '🗑';
            }, 1400);
            return;
          }

          const fallback = categories.find((x) => x.kind === item.kind && x.id !== id)?.id;
          if (!fallback) return;

          tx = tx.map((t) => {
            if (t.categoryId === id) return { ...t, categoryId: fallback };
            return t;
          });

          categories = categories.filter((x) => x.id !== id);
          saveCats();
          saveTx();
          renderCatEditor();
          renderCategorySelect();
          render();
          toast('Kategori dihapus');
        });
      });
    }

    function addCategory() {
      const name = String(($('newCatName').value || '')).trim();
      if (!name) return toast('Nama kategori kosong');

      const base = slugifyLabel(name);
      const id = uniqId(base, (x) => categories.some((c) => c.id === x));
      const emoji = String(($('newCatEmoji').value || '')).trim() || '🏷️';

      categories.push({ id, label: name, emoji, kind: catViewKind });
      $('newCatName').value = '';
      $('newCatEmoji').value = '';
      saveCats();
      renderCatEditor();
      renderCategorySelect();
      render();
      toast('Kategori ditambah');
    }

    function saveCatsFromEditor() {
      const emojiInputs = Array.from($('catList').querySelectorAll('input[data-id-emoji]'));
      const inputs = Array.from($('catList').querySelectorAll('input[data-id]'));
      const next = categories.map((c) => ({ ...c, emoji: (typeof c.emoji === 'string' ? c.emoji : ''), kind: (c.kind || inferCatKind(c.label, c.id)) }));

      for (const inp of emojiInputs) {
        const id = inp.getAttribute('data-id-emoji');
        const v = String((inp.value || '')).trim();
        const item = next.find((x) => x.id === id);
        if (!item) continue;
        item.emoji = v;
      }

      for (const inp of inputs) {
        const id = inp.getAttribute('data-id');
        const v = String((inp.value || '')).trim();
        const item = next.find((x) => x.id === id);
        if (!item) continue;
        item.label = v || item.label;
      }

      categories = next;
      ensureTransferCategory();
      saveCats();
      closeCatModal();
      renderCategorySelect();
      render();
      toast('Tersimpan');
    }

    // ===== Events =====
    function openTxModal(){
      $('txMask').classList.add('show');
      $('txModal').classList.add('show');
      $('txModal').setAttribute('aria-hidden','false');

      $('accTypeMask').classList.remove('show');
      $('accTypeModal').classList.remove('show');
      $('catMask').classList.remove('show');
      $('catModal').classList.remove('show');

      $('date').value = $('date').value || todayISO();
      $('type').value = $('type').value || 'income';

      $('type').dispatchEvent(new Event('change'));
      setTimeout(()=>{ try{ $('amount').focus(); }catch{} }, 60);
    }

    function closeTxModal(){
      $('txMask').classList.remove('show');
      $('txModal').classList.remove('show');
      $('txModal').setAttribute('aria-hidden','true');
      clearEditMode();
    }

    function openResetModal(){
      openResetConfirm();
    }

    // open add
    $('openAddTab').addEventListener('click', () => {
      clearEditMode();
      resetTxForm();
      openTxModal();
    });

    $('txMask').addEventListener('click', closeTxModal);
    $('closeTxModal').addEventListener('click', closeTxModal);
    $('cancelTxBtn').addEventListener('click', closeTxModal);

    $('addBtn').addEventListener('click', addTx);
    $('search').addEventListener('input', render);
    $('month').addEventListener('change', render);
    $('seedBtn').addEventListener('click', seed);
    $('resetBtn').addEventListener('click', openResetModal);
    $('exportBtn').addEventListener('click', exportCSV);

    // PIN settings (biar tombol Set PIN berguna setelah login)
    $('pinSettingsBtn').addEventListener('click', () => {
      if (!__unlocked) {
        toast('Login dulu');
        showLock('login');
        return;
      }
      __pinMode = 'set';
      __pinTarget = 'pin';
      showLock('set');
    });

    // Logout = kunci ulang tanpa refresh
    $('logoutBtn').addEventListener('click', () => {
      if (!__unlocked) return;
      __unlocked = false;
      $('appWrap').classList.add('hidden');
      toast('Aplikasi dikunci');
      showLock('login');
    });

    // detail modal
    $('txDetailMask').addEventListener('click', closeTxDetail);
    $('closeTxDetail').addEventListener('click', closeTxDetail);
    $('txDetailCloseBtn').addEventListener('click', closeTxDetail);
    $('txDetailEditBtn').addEventListener('click', () => {
      if (!detailTxId) return;
      const id = detailTxId;
      closeTxDetail();
      startEditTx(id);
    });
    $('txDetailDeleteBtn').addEventListener('click', () => {
      if (!detailTxId) return;
      const btn = $('txDetailDeleteBtn');
      if (btn.dataset.stage !== 'confirm') {
        btn.dataset.stage = 'confirm';
        btn.textContent = 'Hapus? Klik sekali lagi';
        toast('Klik sekali lagi untuk hapus');
        clearTimeout(window.__delTxTimer);
        window.__delTxTimer = setTimeout(() => {
          btn.dataset.stage = '';
          btn.textContent = 'Hapus transaksi';
        }, 1400);
        return;
      }
      const id = detailTxId;
      closeTxDetail();
      deleteTxById(id);
    });

    // reset confirm
    $('resetMask').addEventListener('click', closeResetConfirm);
    $('closeResetModal').addEventListener('click', closeResetConfirm);
    $('cancelResetBtn').addEventListener('click', closeResetConfirm);
    $('confirmResetBtn').addEventListener('click', () => {
      closeResetConfirm();
      resetAll();
    });

    window.addEventListener('keydown', (e) => {
      if (e.key === 'Escape') {
        // Kalau sedang lock, jangan tutup (biar aman)
        if ($('lockModal')?.classList.contains('show')) return;
        closeResetConfirm();
        closeTxDetail();
        closeTxModal();
        closeAccTypeModal();
        closeCatModal();
      }
    });

    // type change
    $('type').addEventListener('change', () => {
      const v = $('type').value;

      const catField = $('categoryField');
      const catSel = $('category');

      if (v === 'transfer') {
        $('singleAcctField').classList.add('hidden');
        $('transferFromField').classList.remove('hidden');
        $('transferToField').classList.remove('hidden');

        // remember last selected non-transfer category
        if (catSel.value && catKindOf(catSel.value) !== 'transfer') {
          const k = catKindOf(catSel.value);
          if (k === 'income') lastIncomeCatId = catSel.value;
          if (k === 'expense') lastExpenseCatId = catSel.value;
        }

        const transferCatId = ensureTransferCategory();
        catSel.value = transferCatId;
        catSel.disabled = true;
        if (catField) catField.classList.add('hidden');

        $('transferFrom').value = $('transferFrom').value || (accountTypes[0]?.id || 'cash');
        $('transferTo').value = $('transferTo').value || (accountTypes[1]?.id || accountTypes[0]?.id || 'cash');
        return;
      }

      $('singleAcctField').classList.remove('hidden');
      $('transferFromField').classList.add('hidden');
      $('transferToField').classList.add('hidden');

      if (catField) catField.classList.remove('hidden');
      catSel.disabled = false;

      renderCategorySelect();

      // reselect last kind
      const wantKind = (v === 'income') ? 'income' : 'expense';
      const want = (wantKind === 'income') ? lastIncomeCatId : lastExpenseCatId;
      if (want && Array.from(catSel.options).some((o)=>o.value===want)) {
        catSel.value = want;
      }
    });

    // manage akun
    $('manageAccTypesBtn').addEventListener('click', openAccTypeModal);
    $('accTypeMask').addEventListener('click', closeAccTypeModal);
    $('closeAccTypeModal').addEventListener('click', closeAccTypeModal);
    $('cancelAccTypeBtn').addEventListener('click', closeAccTypeModal);
    $('addAccTypeBtn').addEventListener('click', addAccountType);
    $('saveAccTypeBtn').addEventListener('click', saveAccountTypesFromEditor);

    // manage kategori
    $('manageCatsTopBtn').addEventListener('click', openCatModal);
    $('catMask').addEventListener('click', closeCatModal);
    $('closeCatModal').addEventListener('click', closeCatModal);
    $('cancelCatBtn').addEventListener('click', closeCatModal);
    $('addCatBtn').addEventListener('click', addCategory);
    $('saveCatBtn').addEventListener('click', saveCatsFromEditor);

    // ===== PIN Lock wiring =====
    let __pinMode = 'auto'; // 'login' | 'set'
    let __pinTarget = 'pin'; // 'pin' | 'recovery'
    let __unlocked = false; // session unlock (tidak disimpan permanen)

    function showLock(mode){
      __pinMode = mode || 'auto';
      const hasPin = !!loadPinRecord();

      // Jika sudah ada PIN, ubah PIN hanya boleh setelah login
      let m = (mode === 'set') ? 'set' : (mode === 'login' ? 'login' : (hasPin ? 'login' : 'set'));
      if (hasPin && m === 'set' && !__unlocked) m = 'login';

      const pinInput = $('pinInput');
      const pinSubmit = $('pinSubmitBtn');
      const pinModeBtn = $('pinModeBtn');
      const pinTargetBtn = $('pinTargetBtn');
      const pinHint = $('pinHint');
      const pinSub = $('lockSub');
      const resetAllBtn = $('pinResetAllBtn');

      pinInput.value = '';
      pinHint.textContent = '';

      if (m === 'set') {
        // Mode set: bisa pilih PIN Utama / Recovery PIN
        $('lockModal').querySelector('.lockActions')?.classList.add('three');
        pinTargetBtn.classList.remove('hidden');

        const targetLabel = (__pinTarget === 'recovery') ? 'PIN: Recovery' : 'PIN: Utama';
        pinTargetBtn.textContent = targetLabel;

        if (__pinTarget === 'recovery') {
          pinSub.textContent = hasPin ? 'Buat / ganti Recovery PIN (untuk masuk jika lupa PIN utama).' : 'Buat PIN utama dulu sebelum membuat Recovery PIN.';
          pinSubmit.textContent = 'Simpan Recovery';
        } else {
          pinSub.textContent = hasPin ? 'Ganti PIN utama (butuh login dulu).' : 'Buat PIN baru untuk mengunci catatan.';
          pinSubmit.textContent = 'Simpan PIN';
        }

        pinModeBtn.textContent = 'Mode Login';
        resetAllBtn.classList.add('hidden');
      } else {
        $('lockModal').querySelector('.lockActions')?.classList.remove('three');
        pinTargetBtn.classList.add('hidden');
        pinSub.textContent = loadRecoveryRecord() ? 'Masukkan PIN untuk membuka. Jika lupa PIN, kamu bisa pakai Recovery PIN.' : 'Masukkan PIN untuk membuka catatan keuangan.';
        pinSubmit.textContent = 'Masuk';
        pinModeBtn.textContent = 'Set PIN';
        resetAllBtn.classList.toggle('hidden', !hasPin);
      }

      $('lockMask').classList.add('show');
      $('lockModal').classList.add('show');
      $('lockModal').setAttribute('aria-hidden','false');
      document.body.classList.add('locked');
      setTimeout(()=>{ try{ pinInput.focus(); }catch{} }, 60);
    }

    function hideLock(){
      $('lockMask').classList.remove('show');
      $('lockModal').classList.remove('show');
      $('lockModal').setAttribute('aria-hidden','true');
      document.body.classList.remove('locked');
      $('appWrap').classList.remove('hidden');
      __unlocked = true;
    }

    async function handlePinSubmit(){
      const hasPin = !!loadPinRecord();
      const desired = (__pinMode === 'set') ? 'set' : (__pinMode === 'login' ? 'login' : (hasPin ? 'login' : 'set'));
      const pin = String(($('pinInput').value || '')).trim();

      try{
        if (desired === 'set') {
          if (__pinTarget === 'recovery') {
            if (!hasPin) throw new Error('Buat PIN utama dulu');
            await setRecoveryPin(pin);
            $('pinHint').textContent = 'Recovery PIN tersimpan.';
          } else {
            await setPin(pin);
            $('pinHint').textContent = hasPin ? 'PIN utama diperbarui.' : 'PIN tersimpan. Silakan login.';
          }
          $('pinHint').style.color = 'rgba(34,197,94,.95)';

          // Kalau set PIN pertama kali: paksa login. Kalau sedang ganti saat sudah unlock: tutup saja.
          if (!hasPin) { showLock('login'); return; }
          hideLock();
          toast(__pinTarget === 'recovery' ? 'Recovery PIN disimpan' : 'PIN disimpan');
          return;
        }

        const res = await verifyPin(pin);
        if (!res.ok) {
          $('pinHint').textContent = 'PIN salah. Coba lagi.';
          $('pinHint').style.color = 'rgba(248,113,113,.95)';
          return;
        }

        hideLock();
        toast(res.via === 'recovery' ? 'Masuk dengan Recovery PIN' : 'Berhasil login');
        if (res.via === 'recovery') {
          toast('Saran: segera ganti PIN utama');
        }
      }catch(e){
        $('pinHint').textContent = String(e?.message || 'Gagal');
        $('pinHint').style.color = 'rgba(248,113,113,.95)';
      }
    }

    function bindLockUi(){
      $('pinSubmitBtn').addEventListener('click', () => { handlePinSubmit(); });
      $('pinInput').addEventListener('keydown', (e)=>{ if (e.key === 'Enter') handlePinSubmit(); });

      $('pinModeBtn').addEventListener('click', () => {
        const hasPin = !!loadPinRecord();
        // kalau sudah ada PIN tapi belum unlock, jangan izinkan langsung set
        if (hasPin && !__unlocked && __pinMode !== 'login') {
          toast('Login dulu untuk ubah PIN');
          showLock('login');
          return;
        }
        const next = (__pinMode === 'set') ? 'login' : 'set';
        showLock(next);
      });

      $('pinTargetBtn').addEventListener('click', () => {
        __pinTarget = (__pinTarget === 'pin') ? 'recovery' : 'pin';
        showLock('set');
      });
      $('pinResetAllBtn').addEventListener('click', () => {
        const btn = $('pinResetAllBtn');
        if (btn.dataset.stage !== 'confirm') {
          btn.dataset.stage = 'confirm';
          btn.textContent = 'Yakin? Klik sekali lagi untuk reset total';
          toast('Konfirmasi reset total');
          clearTimeout(window.__pinResetTimer);
          window.__pinResetTimer = setTimeout(()=>{
            btn.dataset.stage = '';
            btn.textContent = 'Lupa PIN? Reset semua data';
          }, 1600);
          return;
        }
        clearAllData();
        location.reload();
      });

      // lock screen shouldn't close on mask click (security)
      $('lockMask').addEventListener('click', () => {
        toast('Masukkan PIN untuk membuka');
      });
    }

    // ===== Init =====
    bindLockUi();

    $('date').value = todayISO();
    render();

    // Gate app behind PIN
    if (loadPinRecord()) showLock('login');
    else showLock('set');


    // Floating Add (single source)
    (function setupAddFab(){
      const btn = $('openAddTab');
      const slot = $('addBtnSlot');
      if (!btn || !slot) return;

      let normalHeight = btn.getBoundingClientRect().height || 56;

      const recalc = () => {
        const wasFab = btn.classList.contains('fab');
        if (wasFab) btn.classList.remove('fab');
        normalHeight = btn.getBoundingClientRect().height || normalHeight;
        if (wasFab) btn.classList.add('fab');
        if (wasFab) slot.style.height = normalHeight + 'px';
      };

      const apply = (isFab) => {
        btn.classList.toggle('fab', !!isFab);
        slot.style.height = isFab ? (normalHeight + 'px') : '';
      };

      apply(false);

      if ('IntersectionObserver' in window) {
        const obs = new IntersectionObserver((entries) => {
          const e = entries[0];
          const visible = e.isIntersecting && e.intersectionRatio > 0.6;
          apply(!visible);
        }, { threshold: [0, 0.35, 0.6, 1] });

        obs.observe(slot);
      } else {
        window.addEventListener('scroll', () => {
          const r = slot.getBoundingClientRect();
          const visible = r.top >= 0 && r.bottom <= (window.innerHeight || document.documentElement.clientHeight);
          apply(!visible);
        }, { passive: true });
      }

      window.addEventListener('resize', recalc, { passive: true });
      setTimeout(recalc, 60);
    })();

    // ===== Self-tests (ringan) =====
    (function selfTest(){
      try{
        console.assert(csvEscape('a,b') === '"a,b"', 'csvEscape comma');
        console.assert(csvEscape('a"b') === '"a""b"', 'csvEscape quote');
        console.assert(csvEscape('a\nb') === '"a\nb"', 'csvEscape newline');
        console.assert(csvEscape('a\rb') === '"a\rb"', 'csvEscape CR');
        console.assert(csvEscape('a\r\nb') === '"a\r\nb"', 'csvEscape CRLF');

        const sample = [['A','B'],['1','2']];
        const csv = '\uFEFF' + sample.map(r => r.map(csvEscape).join(',')).join('\r\n');
        console.assert(csv.includes('\r\n'), 'csv join CRLF');

        const transferId = ensureCategory('Transfer');
        console.assert(!!transferId, 'ensureCategory transfer');
        console.assert(catKindOf(transferId) === 'transfer', 'transfer kind');

        console.assert(categories.some((c)=>c.kind==='income'), 'has income cats');
        console.assert(categories.some((c)=>c.kind==='expense'), 'has expense cats');

        console.assert(typeof render === 'function', 'render exists');
        render();

        console.assert(typeof acctLabel('cash') === 'string', 'acctLabel string');
        console.assert(typeof catLabel(transferId) === 'string', 'catLabel string');
      }catch(e){
        console.warn('Self-test failed', e);
      }
    })();
  </script>
</body>
</html>
