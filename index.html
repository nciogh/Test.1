import React, { useState, useEffect } from 'react';
import { AlertCircle, ChevronDown, ChevronUp, CheckCircle2 } from 'lucide-react';

const quartets = [
  [ { text: "Entusiasta", type: "PR" }, { text: "Decidido", type: "CO" }, { text: "Concienzudo", type: "AN" }, { text: "Leal", type: "FA" } ],
  [ { text: "Reservado", type: "AN" }, { text: "Simpático", type: "PR" }, { text: "Bondadoso", type: "FA" }, { text: "Intranquilo", type: "CO" } ],
  [ { text: "Reflexivo", type: "FA" }, { text: "Sociable", type: "PR" }, { text: "Exigente", type: "CO" }, { text: "Prudente", type: "AN" } ],
  [ { text: "Enérgico", type: "CO" }, { text: "Diplomático, con tacto", type: "AN" }, { text: "Compasivo", type: "FA" }, { text: "Alegre", type: "PR" } ],
  [ { text: "Servicial", type: "FA" }, { text: "Reflexivo", type: "AN" }, { text: "Hablador", type: "PR" }, { text: "Impulsor, animador", type: "CO" } ],
  [ { text: "Competitivo", type: "CO" }, { text: "Ecuánime", type: "FA" }, { text: "Sociable", type: "PR" }, { text: "Metódico, concienzudo", type: "AN" } ],
  [ { text: "Amable, afable", type: "PR" }, { text: "Agresivo", type: "CO" }, { text: "Lógico", type: "AN" }, { text: "Relajado", type: "FA" } ],
  [ { text: "Controlado, contenido", type: "AN" }, { text: "Simpático", type: "PR" }, { text: "Atento, educado", type: "FA" }, { text: "Cabezota, terco", type: "CO" } ],
  [ { text: "Animador", type: "PR" }, { text: "Constante, perseverante", type: "FA" }, { text: "Obstinado", type: "CO" }, { text: "Meticuloso", type: "AN" } ],
  [ { text: "Directo", type: "CO" }, { text: "Alegre", type: "PR" }, { text: "Diplomático", type: "FA" }, { text: "Considerado, respetuoso", type: "AN" } ]
];

export default function App() {
  // Inicializamos el estado para almacenar las respuestas (10 grupos, 4 respuestas cada uno)
  const [scores, setScores] = useState(
    Array(10).fill(null).map(() => ({ 0: '', 1: '', 2: '', 3: '' }))
  );
  
  const [error, setError] = useState('');
  const [showResults, setShowResults] = useState(false);
  const [showDetails, setShowDetails] = useState(false);
  const [totals, setTotals] = useState({ CO: 0, PR: 0, FA: 0, AN: 0 });

  // Maneja la selección de un número
  const handleSelect = (groupIndex, adjIndex, num) => {
    const newScores = [...scores];
    
    // Si hace clic en el mismo número, lo desmarca
    if (newScores[groupIndex][adjIndex] === num) {
      newScores[groupIndex][adjIndex] = '';
    } else {
      // Si el número ya estaba en otro adjetivo del mismo grupo, lo quita de allí (previene duplicados)
      Object.keys(newScores[groupIndex]).forEach(key => {
        if (newScores[groupIndex][key] === num) {
          newScores[groupIndex][key] = '';
        }
      });
      // Asigna el nuevo número
      newScores[groupIndex][adjIndex] = num;
    }
    
    setScores(newScores);
    setError('');
    setShowResults(false);
  };

  const calculateResults = () => {
    // Validación: verificar que todos los grupos estén completos
    for (let i = 0; i < 10; i++) {
      const group = scores[i];
      const values = Object.values(group).filter(v => v !== '');
      if (values.length !== 4) {
        setError(`Por favor, completa todas las opciones en el Grupo ${i + 1}. Faltan asignar números.`);
        // Hacer scroll suave hacia el error
        window.scrollTo({ top: 0, behavior: 'smooth' });
        return;
      }
    }

    // Calcular totales
    const newTotals = { CO: 0, PR: 0, FA: 0, AN: 0 };
    scores.forEach((group, gIndex) => {
      Object.entries(group).forEach(([aIndex, val]) => {
        const type = quartets[gIndex][aIndex].type;
        newTotals[type] += val;
      });
    });

    setTotals(newTotals);
    setShowResults(true);
    setError('');
    
    // Scroll hacia los resultados
    setTimeout(() => {
      document.getElementById('resultados-section')?.scrollIntoView({ behavior: 'smooth' });
    }, 100);
  };

  // Calcula el progreso para la barra superior
  const getProgress = () => {
    let answered = 0;
    scores.forEach(group => {
      answered += Object.values(group).filter(v => v !== '').length;
    });
    return (answered / 40) * 100;
  };

  return (
    <div className="min-h-screen bg-[#f8fafc] text-slate-800 pb-16 font-sans">
      {/* Barra de progreso fija arriba */}
      <div className="fixed top-0 left-0 w-full h-1.5 bg-slate-200 z-50">
        <div 
          className="h-full bg-blue-600 transition-all duration-300 ease-out"
          style={{ width: `${getProgress()}%` }}
        ></div>
      </div>

      <div className="max-w-4xl mx-auto pt-12 px-4 sm:px-6">
        
        <header className="text-center mb-10">
          <h1 className="text-3xl sm:text-4xl font-bold tracking-tight text-slate-900 mb-4">
            Test de Estilos Sociales
          </h1>
          <p className="text-slate-500 max-w-2xl mx-auto text-sm sm:text-base leading-relaxed">
            Establece un ranking en cada grupo de adjetivos. Selecciona <strong className="text-slate-700">4</strong> para el que más te describe, hasta <strong className="text-slate-700">1</strong> para el que menos. Usa cada número una sola vez por grupo.
          </p>
        </header>

        {error && (
          <div className="mb-8 p-4 bg-red-50 border border-red-200 rounded-xl flex items-start gap-3 text-red-700 animate-in fade-in">
            <AlertCircle className="w-5 h-5 flex-shrink-0 mt-0.5" />
            <p className="font-medium text-sm">{error}</p>
          </div>
        )}

        <div className="flex flex-col gap-6 max-w-2xl mx-auto">
          {quartets.map((group, gIndex) => {
            const isGroupComplete = Object.values(scores[gIndex]).filter(v => v !== '').length === 4;
            
            return (
              <div 
                key={gIndex} 
                className={`bg-white rounded-2xl p-6 shadow-sm border transition-colors duration-300 ${isGroupComplete ? 'border-green-200 bg-green-50/10' : 'border-slate-200'}`}
              >
                <div className="flex items-center justify-between mb-5">
                  <h3 className="text-xs font-bold text-slate-400 uppercase tracking-wider">
                    Grupo {gIndex + 1}
                  </h3>
                  {isGroupComplete && <CheckCircle2 className="w-4 h-4 text-green-500" />}
                </div>
                
                <div className="space-y-4">
                  {group.map((adj, aIndex) => (
                    <div key={aIndex} className="flex flex-col sm:flex-row sm:items-center justify-between gap-3">
                      <label className="text-sm font-medium text-slate-700 flex-1">
                        {adj.text}
                      </label>
                      <div className="flex gap-1.5 shrink-0">
                        {[1, 2, 3, 4].map(num => {
                          const isSelected = scores[gIndex][aIndex] === num;
                          // Check if this number is selected somewhere else in this group
                          const isUsedInGroup = Object.values(scores[gIndex]).includes(num);
                          
                          return (
                            <button
                              key={num}
                              onClick={() => handleSelect(gIndex, aIndex, num)}
                              className={`
                                w-10 h-10 sm:w-9 sm:h-9 rounded-full text-sm font-semibold transition-all duration-200
                                flex items-center justify-center focus:outline-none focus:ring-2 focus:ring-offset-1 focus:ring-blue-500
                                ${isSelected 
                                  ? 'bg-blue-600 text-white shadow-md scale-105' 
                                  : isUsedInGroup
                                    ? 'bg-slate-50 text-slate-300 cursor-not-allowed border border-slate-100' // Number used in another row
                                    : 'bg-slate-100 text-slate-600 hover:bg-slate-200 hover:text-slate-800'
                                }
                              `}
                            >
                              {num}
                            </button>
                          );
                        })}
                      </div>
                    </div>
                  ))}
                </div>
              </div>
            );
          })}
        </div>

        <div className="mt-12 flex flex-col items-center">
          <button
            onClick={calculateResults}
            className="bg-slate-900 hover:bg-slate-800 text-white font-medium py-3.5 px-10 rounded-xl shadow-lg hover:shadow-xl transition-all duration-200 w-full sm:w-auto text-lg flex items-center justify-center gap-2"
          >
            Generar Resultados
          </button>
        </div>

        {/* Sección de Resultados */}
        {showResults && (
          <div id="resultados-section" className="mt-16 animate-in slide-in-from-bottom-8 fade-in duration-500">
            <div className="bg-white p-8 rounded-3xl shadow-sm border border-slate-200">
              <h2 className="text-2xl font-bold mb-8 text-center text-slate-800">Tus Resultados Finales</h2>
              
              <div className="grid grid-cols-2 md:grid-cols-4 gap-4 sm:gap-6">
                {[
                  { id: 'CO', color: 'bg-blue-50 border-blue-100 text-blue-700', label: 'CO' },
                  { id: 'PR', color: 'bg-emerald-50 border-emerald-100 text-emerald-700', label: 'PR' },
                  { id: 'FA', color: 'bg-amber-50 border-amber-100 text-amber-700', label: 'FA' },
                  { id: 'AN', color: 'bg-purple-50 border-purple-100 text-purple-700', label: 'AN' }
                ].map(type => (
                  <div key={type.id} className={`${type.color} border rounded-2xl p-6 text-center flex flex-col items-center justify-center`}>
                    <span className="text-sm font-bold opacity-70 mb-1">{type.label}</span>
                    <span className="text-4xl font-black">{totals[type.id]}</span>
                  </div>
                ))}
              </div>

              {/* Botón secundario para ver detalles */}
              <div className="mt-10 border-t border-slate-100 pt-6 text-center">
                <button
                  onClick={() => setShowDetails(!showDetails)}
                  className="inline-flex items-center gap-2 text-sm font-medium text-slate-500 hover:text-slate-800 transition-colors"
                >
                  {showDetails ? 'Ocultar detalle de respuestas' : 'Ver detalle de mis respuestas'}
                  {showDetails ? <ChevronUp className="w-4 h-4" /> : <ChevronDown className="w-4 h-4" />}
                </button>
              </div>

              {/* Acordeón de detalles */}
              {showDetails && (
                <div className="mt-6 text-sm text-slate-600 bg-slate-50 rounded-xl p-6 border border-slate-100 grid grid-cols-1 sm:grid-cols-2 gap-x-8 gap-y-6">
                  {quartets.map((group, gIndex) => (
                    <div key={`detail-${gIndex}`}>
                      <h4 className="font-semibold text-slate-800 mb-2 border-b border-slate-200 pb-1">Grupo {gIndex + 1}</h4>
                      <ul className="space-y-1.5">
                        {/* Sort by score descending (4 to 1) for better readability */}
                        {[4, 3, 2, 1].map(num => {
                          const adjIndex = Object.keys(scores[gIndex]).find(key => scores[gIndex][key] === num);
                          if (adjIndex !== undefined) {
                            const adj = group[adjIndex];
                            return (
                              <li key={num} className="flex justify-between items-center">
                                <span><span className="font-medium text-slate-400 mr-2">{num}</span> {adj.text}</span>
                                <span className="text-xs font-bold px-2 py-0.5 bg-slate-200 rounded text-slate-600">{adj.type}</span>
                              </li>
                            );
                          }
                          return null;
                        })}
                      </ul>
                    </div>
                  ))}
                </div>
              )}

            </div>
          </div>
        )}

      </div>
    </div>
  );
}
