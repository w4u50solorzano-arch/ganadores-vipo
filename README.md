<!doctype html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
    <title>Ganadores VIP - Pronósticos de Animalitos</title>
    <meta name="description" content="Acceso exclusivo a pronósticos premium y planes de inversión." />
    <meta name="theme-color" content="#0f172a" />
    
    <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>👑</text></svg>" />

    <script src="https://cdn.tailwindcss.com"></script>

    <style>
      /* Estilos base extraídos de tu configuración */
      body {
        background-color: #0f172a;
        color: white;
        margin: 0;
        font-family: system-ui, -apple-system, sans-serif;
      }
      #root {
        min-height: 100vh;
      }
    </style>
  </head>
  <body>
    <div id="root"></div>

    <script src="https://unpkg.com/react@18/umd/react.production.min.js"></script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js"></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>

    <script type="text/babel">
      const { useState } = React;

      function App() {
        return (
          <div className="flex flex-col min-h-screen items-center justify-center p-6 text-center">
            <header className="mb-8 animate-fade-in">
              <div className="text-6xl mb-4">👑</div>
              <h1 className="text-4xl font-extrabold text-yellow-500 mb-2">
                Ganadores VIP
              </h1>
              <p className="text-gray-400 text-lg">
                Acceso exclusivo a pronósticos premium y planes de inversión.
              </p>
            </header>

            <main className="w-full max-w-md bg-slate-800/50 p-6 rounded-2xl border border-slate-700 shadow-2xl backdrop-blur-sm">
              <h2 className="text-xl font-semibold mb-4 text-white uppercase tracking-wider">Pronósticos del Día</h2>
              
              <div className="grid grid-cols-2 gap-4">
                <div className="bg-slate-700/50 p-4 rounded-lg border border-slate-600">
                  <span className="block text-xs text-yellow-500 uppercase font-bold mb-1">Lotto Activo</span>
                  <span className="text-2xl font-bold">⏳...</span>
                </div>
                <div className="bg-slate-700/50 p-4 rounded-lg border border-slate-600">
                  <span className="block text-xs text-yellow-500 uppercase font-bold mb-1">La Granjita</span>
                  <span className="text-2xl font-bold">⏳...</span>
                </div>
              </div>
              
              <button className="w-full mt-6 bg-gradient-to-r from-yellow-600 to-yellow-500 hover:from-yellow-500 hover:to-yellow-400 text-white font-bold py-4 rounded-xl shadow-lg transform active:scale-95 transition-all">
                ACCEDER A DATOS VIP
              </button>
            </main>

            <footer className="mt-auto py-8 text-slate-500 text-xs italic">
              &copy; 2026 Ganadores VIP - Todos los derechos reservados.
            </footer>
          </div>
        );
      }

      // Renderizado final
      const root = ReactDOM.createRoot(document.getElementById('root'));
      root.render(<App />);
    </script>
  </body>
</html>
