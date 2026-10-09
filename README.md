# Gift-market
<!DOCTYPE html>
<html lang="ru" class="dark">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Gift Radar — Агрегатор подарков Telegram</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script>
    tailwind.config = {
      darkMode: 'class',
      theme: {
        extend: {
          colors: {
            darkBg: '#0f172a',
            cardBg: '#1e293b',
            accent: '#38bdf8',
          }
        }
      }
    }
  </script>
</head>
<body class="bg-darkBg text-slate-100 min-h-screen font-sans">

  <!-- Header -->
  <header class="border-b border-slate-800 bg-slate-900/80 backdrop-blur sticky top-0 z-50 px-6 py-4 flex justify-between items-center">
    <div class="flex items-center space-x-3">
      <span class="text-2xl">🎁</span>
      <h1 class="text-xl font-bold tracking-tight">Gift<span class="text-accent">Radar</span></h1>
      <span class="text-xs bg-emerald-500/10 text-emerald-400 border border-emerald-500/20 px-2 py-0.5 rounded-full">Live Feed</span>
    </div>

    <div class="flex items-center space-x-4">
      <button class="bg-accent text-slate-950 font-semibold px-4 py-2 rounded-lg text-sm hover:bg-sky-400 transition">
        Подключить TON Кошелек
      </button>
    </div>
  </header>

  <main class="max-w-7xl mx-auto p-6 space-y-6">

    <!-- Статистика / Метрики рынка -->
    <div class="grid grid-cols-1 md:grid-cols-4 gap-4">
      <div class="bg-cardBg p-4 rounded-xl border border-slate-800">
        <p class="text-xs text-slate-400">Объем 24ч</p>
        <p class="text-2xl font-bold mt-1">42,580 TON</p>
        <span class="text-xs text-emerald-400">+14.2%</span>
      </div>
      <div class="bg-cardBg p-4 rounded-xl border border-slate-800">
        <p class="text-xs text-slate-400">Активных ордеров</p>
        <p class="text-2xl font-bold mt-1">1,420</p>
        <span class="text-xs text-slate-500">На 6 маркетах</span>
      </div>
      <div class="bg-cardBg p-4 rounded-xl border border-slate-800">
        <p class="text-xs text-slate-400">Лучший спред</p>
        <p class="text-2xl font-bold mt-1">~1.2%</p>
        <span class="text-xs text-accent">Высокая ликвидность</span>
      </div>
      <div class="bg-cardBg p-4 rounded-xl border border-slate-800">
        <p class="text-xs text-slate-400">Скорость обновления</p>
        <p class="text-2xl font-bold mt-1 text-emerald-400">~250 мс</p>
        <span class="text-xs text-slate-500">WebSocket Online</span>
      </div>
    </div>

    <!-- Фильтры и поиск -->
    <div class="flex flex-wrap items-center justify-between gap-4 bg-cardBg p-4 rounded-xl border border-slate-800">
      <div class="flex items-center gap-3">
        <input 
          type="text" 
          placeholder="Поиск подарка (напр. Durov's Cap, Plush Bear)..." 
          class="bg-slate-900 border border-slate-700 px-4 py-2 rounded-lg text-sm w-72 focus:outline-none focus:border-accent"
        />
        <select class="bg-slate-900 border border-slate-700 px-3 py-2 rounded-lg text-sm">
          <option>Все маркеты</option>
          <option>Getgems</option>
          <option>Tonnel</option>
          <option>P2P Orders</option>
        </select>
      </div>
      <div class="flex items-center gap-2">
