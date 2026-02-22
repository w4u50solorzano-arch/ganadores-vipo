<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
    <title>Ganadores VIP - Pronósticos de Animalitos</title>
    <meta name="description" content="Acceso exclusivo a pronósticos premium y planes de inversión." />
    <meta name="theme-color" content="#0f172a" />
    <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>👑</text></svg>" />
    
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://unpkg.com/lucide@latest"></script>

    <style>
      /* Estilos base de tu index.css */
      body { background-color: #0f172a; color: white; margin: 0; font-family: ui-sans-serif, system-ui, sans-serif; }
      .glass-card { background: rgba(30, 41, 59, 0.7); backdrop-filter: blur(10px); border: 1px solid rgba(51, 65, 85, 1); }
      .gold-gradient { background: linear-gradient(135deg, #fbbf24 0%, #d97706 100%); }
    </style>
  </head>
  <body>
    <div id="root"></div>

    <script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

    <script type="text/babel">
      const { useState, useEffect } = React;

      // Componentes portados de tu App.tsx
      const App = () => {
        const [activeTab, setActiveTab] = useState('lotteries');

        return (
          <div className="min-h-screen pb-20">
            {/* Header VIP */}
            <header className="p-6 text-center border-b border-slate-800 bg-slate-900/50 sticky top-0 z-10 backdrop-blur-md">
              <div className="inline-block p-3 rounded-2xl bg-yellow-500/10 mb-3">
                <span className="text-3xl">👑</span>
              </div>
              <h1 className="text-2xl font-black text-yellow-500 uppercase tracking-tighter">Ganadores VIP</h1>
              <p className="text-slate-400 text-xs">Pronósticos Premium & Inversión</p>
            </header>

            <main className="p-4 max-w-md mx-auto space-y-6">
              {activeTab === 'lotteries' && (
                <div className="space-y-4 animate-in fade-in duration-500">
                  <h2 className="text-lg font-bold flex items-center gap-2"><span className="text-yellow-500">🎯</span> Loterías Disponibles</h2>
                  <div className="grid gap-3">
                    {['Lotto Activo', 'La Granjita', 'Lotto Rey', 'Granjita Terminal'].map(lottery => (
                      <div key={lottery} className="glass-card p-4 rounded-2xl flex justify-between items-center hover:border-yellow-500/50 transition-colors">
                        <span className="font-semibold">{lottery}</span>
                        <span className="text-xs bg-green-500/20 text-green-400 px-2 py-1 rounded-full font-bold uppercase">Activo</span>
                      </div>
                    ))}
                  </div>
                </div>
              )}

              {activeTab === 'results' && (
                <div className="space-y-4 animate-in slide-in-from-bottom-4 duration-500">
                  <h2 className="text-lg font-bold flex items-center gap-2"><span className="text-yellow-500">📊</span> Últimos Resultados</h2>
                  <div className="glass-card rounded-3xl overflow-hidden">
                    <div className="p-4 bg-slate-700/30 border-b border-slate-700 flex justify-between">
                      <span className="font-bold text-yellow-500">Lotto Activo</span>
                      <span className="text-slate-400">9:00 AM</span>
                    </div>
                    <div className="p-8 text-center">
                      <div className="text-6xl mb-2">🦅</div>
                      <p className="text-xl font-bold tracking-widest">ÁGUILA (09)</p>
                    </div>
                  </div>
                </div>
              )}

              {activeTab === 'premium' && (
                <div className="space-y-4 animate-in zoom-in duration-500">
                  <div className="gold-gradient p-6 rounded-3xl text-slate-900 text-center shadow-lg shadow-yellow-600/20">
                    <h2 className="text-2xl font-black mb-1">PLANES VIP</h2>
                    <p className="font-medium opacity-90 mb-4 text-sm">Multiplica tus ganancias hoy mismo</p>
                    <button className="bg-slate-900 text-white w-full py-3 rounded-xl font-bold shadow-xl">VER PLANES DE INVERSIÓN</button>
                  </div>
                </div>
              )}
            </main>

            {/* Navegación Inferior */}
            <nav className="fixed bottom-0 left-0 right-0 glass-card border-t border-slate-700 p-2 flex justify-around items-center rounded-t-3xl shadow-2xl z-20">
              <button onClick={() => setActiveTab('lotteries')} className={`p-3 rounded-xl transition-all ${activeTab === 'lotteries' ? 'text-yellow-500 bg-yellow-500/10 scale-110' : 'text-slate-500'}`}>
                <span className="block text-[20px]">🎯</span>
                <span className="text-[10px] font-bold uppercase mt-1">Sorteos</span>
              </button>
              <button onClick={() => setActiveTab('results')} className={`p-3 rounded-xl transition-all ${activeTab === 'results' ? 'text-yellow-500 bg-yellow-500/10 scale-110' : 'text-slate-500'}`}>
                <span className="block text-[20px]">📊</span>
                <span className="text-[10px] font-bold uppercase mt-1">Resultados</span>
              </button>
              <button onClick={() => setActiveTab('premium')} className={`p-3 rounded-xl transition-all ${activeTab === 'premium' ? 'text-yellow-500 bg-yellow-500/10 scale-110' : 'text-slate-500'}`}>
                <span className="block text-[20px]">👑</span>
                <span className="text-[10px] font-bold uppercase mt-1">Premium</span>
              </button>
            </nav>
          </div>
        );
      };

      const root = ReactDOM.createRoot(document.getElementById('root'));
      root.render(<App />);
    </script>
  </body>
</html>
