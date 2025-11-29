import React, { useState, useEffect } from 'react';
import { BarChart, Bar, PieChart, Pie, Cell, XAxis, YAxis, CartesianGrid, Tooltip, Legend, ResponsiveContainer, Label } from 'recharts';

const FoodAnalysisDashboard = () => {
  const [activeChart, setActiveChart] = useState('comparison');
  const [summaryStats, setSummaryStats] = useState(null);
  const [stateWinners, setStateWinners] = useState([]);

  // Raw data from the images
  const rawData = [
    { state: 'Selangor', total: 90476, nasiLemak: 26050, rotiCanai: 22619, nasiGoreng: 12667, charKueyTeow: 10857, satay: 5207, other: 13076 },
    { state: 'Johor', total: 49405, nasiLemak: 13340, rotiCanai: 13586, nasiGoreng: 6917, charKueyTeow: 5929, satay: 2717, other: 6916 },
    { state: 'Sabah', total: 34226, nasiLemak: 9583, rotiCanai: 8557, nasiGoreng: 4792, charKueyTeow: 4107, satay: 1711, other: 5476 },
    { state: 'Kuala Lumpur (W.P.)', total: 28571, nasiLemak: 8229, rotiCanai: 7143, nasiGoreng: 4000, charKueyTeow: 3429, satay: 1644, other: 4126 },
    { state: 'Sarawak', total: 27678, nasiLemak: 7750, rotiCanai: 6919, nasiGoreng: 3875, charKueyTeow: 3321, satay: 1384, other: 4428 },
    { state: 'Perak', total: 27083, nasiLemak: 7583, rotiCanai: 6771, nasiGoreng: 3792, charKueyTeow: 3250, satay: 1354, other: 4333 },
    { state: 'Penang', total: 23512, nasiLemak: 5878, rotiCanai: 6466, nasiGoreng: 3292, charKueyTeow: 3682, satay: 1176, other: 3018 },
    { state: 'Kedah', total: 22619, nasiLemak: 6333, rotiCanai: 5655, nasiGoreng: 3167, charKueyTeow: 2714, satay: 1131, other: 3619 },
    { state: 'Pahang', total: 17298, nasiLemak: 4833, rotiCanai: 4325, nasiGoreng: 2422, charKueyTeow: 2076, satay: 865, other: 2776 },
    { state: 'Kelantan', total: 16071, nasiLemak: 4500, rotiCanai: 4018, nasiGoreng: 2250, charKueyTeow: 1929, satay: 804, other: 2571 },
    { state: 'Negeri Sembilan', total: 13988, nasiLemak: 3917, rotiCanai: 3497, nasiGoreng: 1958, charKueyTeow: 1679, satay: 699, other: 2238 },
    { state: 'Terengganu', total: 11607, nasiLemak: 3250, rotiCanai: 2902, nasiGoreng: 1625, charKueyTeow: 1393, satay: 580, other: 1857 },
    { state: 'Malacca', total: 11012, nasiLemak: 3083, rotiCanai: 2753, nasiGoreng: 1542, charKueyTeow: 1321, satay: 577, other: 1736 },
    { state: 'Perlis', total: 2679, nasiLemak: 750, rotiCanai: 670, nasiGoreng: 375, charKueyTeow: 321, satay: 134, other: 428 },
    { state: 'Putrajaya (W.P.)', total: 1714, nasiLemak: 480, rotiCanai: 429, nasiGoreng: 240, charKueyTeow: 206, satay: 86, other: 274 },
    { state: 'Labuan (W.P.)', total: 1214, nasiLemak: 340, rotiCanai: 304, nasiGoreng: 170, charKueyTeow: 146, satay: 61, other: 193 }
  ];

  // Calculate statistics on mount
  useEffect(() => {
    calculateStats();
  }, []);

  const calculateStats = () => {
    // Calculate national totals
    const totals = {
      nasiLemak: 0,
      rotiCanai: 0,
      nasiGoreng: 0,
      charKueyTeow: 0,
      satay: 0,
      other: 0,
      grandTotal: 0
    };

    rawData.forEach(row => {
      totals.nasiLemak += row.nasiLemak;
      totals.rotiCanai += row.rotiCanai;
      totals.nasiGoreng += row.nasiGoreng;
      totals.charKueyTeow += row.charKueyTeow;
      totals.satay += row.satay;
      totals.other += row.other;
      totals.grandTotal += row.total;
    });

    // Calculate winners per state
    const winners = rawData.map(row => {
      const foods = {
        'Nasi Lemak': row.nasiLemak,
        'Roti Canai': row.rotiCanai,
        'Nasi Goreng': row.nasiGoreng,
        'Char Kuey Teow': row.charKueyTeow,
        'Satay': row.satay,
        'Other': row.other
      };
      const winner = Object.keys(foods).reduce((a, b) => foods[a] > foods[b] ? a : b);
      
      return {
        state: row.state,
        winner: winner,
        value: foods[winner],
        nasiLemak: row.nasiLemak,
        rotiCanai: row.rotiCanai,
        gap: row.nasiLemak - row.rotiCanai
      };
    });

    const nasiLemakWins = winners.filter(w => w.winner === 'Nasi Lemak').length;
    const rotiCanaiWins = winners.filter(w => w.winner === 'Roti Canai').length;

    const stats = {
      nasiLemakTotal: totals.nasiLemak,
      rotiCanaiTotal: totals.rotiCanai,
      nasiLemakShare: (totals.nasiLemak / totals.grandTotal * 100).toFixed(2),
      rotiCanaiShare: (totals.rotiCanai / totals.grandTotal * 100).toFixed(2),
      nasiLemakWins: nasiLemakWins,
      rotiCanaiWins: rotiCanaiWins,
      totalStates: rawData.length,
      isNasiLemakNumber1: totals.nasiLemak > totals.rotiCanai,
      gap: totals.nasiLemak - totals.rotiCanai,
      gapPercentage: ((totals.nasiLemak - totals.rotiCanai) / totals.rotiCanai * 100).toFixed(2)
    };

    setSummaryStats(stats);
    setStateWinners(winners);
  };

  // Prepare data for charts
  const nationalTotals = [
    { name: 'Nasi Lemak', value: rawData.reduce((sum, row) => sum + row.nasiLemak, 0), color: '#FF6B6B' },
    { name: 'Roti Canai', value: rawData.reduce((sum, row) => sum + row.rotiCanai, 0), color: '#4ECDC4' },
    { name: 'Nasi Goreng', value: rawData.reduce((sum, row) => sum + row.nasiGoreng, 0), color: '#FFE66D' },
    { name: 'Char Kuey Teow', value: rawData.reduce((sum, row) => sum + row.charKueyTeow, 0), color: '#95E1D3' },
    { name: 'Satay', value: rawData.reduce((sum, row) => sum + row.satay, 0), color: '#F38181' },
    { name: 'Other', value: rawData.reduce((sum, row) => sum + row.other, 0), color: '#AA96DA' }
  ];

  const top10States = rawData.slice(0, 10);

  const CustomTooltip = ({ active, payload }) => {
    if (active && payload && payload.length) {
      return (
        <div className="bg-white p-4 border-2 border-gray-300 rounded shadow-lg">
          <p className="font-bold text-gray-800">{payload[0].name || payload[0].payload.name}</p>
          {payload.map((entry, index) => (
            <p key={index} style={{ color: entry.color || entry.fill }} className="text-sm">
              {entry.dataKey || 'Value'}: {entry.value.toLocaleString()}k
            </p>
          ))}
        </div>
      );
    }
    return null;
  };

  if (!summaryStats) return <div className="flex items-center justify-center h-screen">Loading...</div>;

  return (
    <div className="min-h-screen bg-gradient-to-br from-purple-600 via-purple-700 to-indigo-800 p-6">
      <div className="max-w-7xl mx-auto">
        {/* Header */}
        <div className="bg-white rounded-2xl shadow-2xl p-10 mb-8 text-center">
          <h1 className="text-5xl font-bold text-purple-600 mb-4">🍽️ Malaysian Food Market Analysis</h1>
          <p className="text-2xl text-gray-600 mb-6">Is Nasi Lemak Really the Best Seller in Malaysia?</p>
          
          <div className={`inline-block px-12 py-4 rounded-full text-2xl font-bold ${
            summaryStats.isNasiLemakNumber1 
              ? 'bg-gradient-to-r from-green-400 to-green-600 text-white animate-pulse' 
              : 'bg-gradient-to-r from-red-400 to-red-600 text-white animate-pulse'
          }`}>
            {summaryStats.isNasiLemakNumber1 
              ? '✅ YES! Nasi Lemak is #1 in Malaysia!' 
              : '❌ NO! Nasi Lemak is NOT #1'}
          </div>
        </div>

        {/* Stats Grid */}
        <div className="grid grid-cols-1 md:grid-cols-4 gap-6 mb-8">
          <div className="bg-gradient-to-br from-green-100 to-green-200 rounded-xl shadow-lg p-6 border-l-4 border-green-500">
            <h3 className="text-purple-700 font-semibold text-lg mb-2">🏆 National Champion</h3>
            <div className="text-4xl font-bold text-gray-800">
              {summaryStats.isNasiLemakNumber1 ? 'Nasi Lemak' : 'Roti Canai'}
            </div>
            <p className="text-gray-600 text-sm mt-2">
              {(summaryStats.isNasiLemakNumber1 ? summaryStats.nasiLemakTotal : summaryStats.rotiCanaiTotal).toLocaleString()}k monthly
            </p>
          </div>

          <div className="bg-white rounded-xl shadow-lg p-6 border-l-4 border-purple-500">
            <h3 className="text-purple-700 font-semibold text-lg mb-2">📈 Market Share</h3>
            <div className="text-4xl font-bold text-gray-800">{summaryStats.nasiLemakShare}%</div>
            <p className="text-gray-600 text-sm mt-2">of total monthly volume</p>
          </div>

          <div className="bg-white rounded-xl shadow-lg p-6 border-l-4 border-blue-500">
            <h3 className="text-purple-700 font-semibold text-lg mb-2">🗺️ States Won</h3>
            <div className="text-4xl font-bold text-gray-800">
              {summaryStats.nasiLemakWins}/{summaryStats.totalStates}
            </div>
            <p className="text-gray-600 text-sm mt-2">states dominated</p>
          </div>

          <div className="bg-white rounded-xl shadow-lg p-6 border-l-4 border-indigo-500">
            <h3 className="text-purple-700 font-semibold text-lg mb-2">📊 Lead Margin</h3>
            <div className="text-4xl font-bold text-gray-800">
              {summaryStats.gap > 0 ? '+' : ''}{summaryStats.gapPercentage}%
            </div>
            <p className="text-gray-600 text-sm mt-2">ahead of 2nd place</p>
          </div>
        </div>

        {/* Chart Controls */}
        <div className="flex flex-wrap justify-center gap-4 mb-8">
          {[
            { id: 'comparison', label: '📊 Food Comparison' },
            { id: 'marketShare', label: '🥧 Market Share' },
            { id: 'stateWinners', label: '🗺️ State Winners' },
            { id: 'topStates', label: '🏅 Top States' },
            { id: 'nasiVsRoti', label: '⚔️ Nasi vs Roti' }
          ].map(btn => (
            <button
              key={btn.id}
              onClick={() => setActiveChart(btn.id)}
              className={`px-8 py-3 rounded-full font-bold text-lg transition-all ${
                activeChart === btn.id
                  ? 'bg-gradient-to-r from-purple-500 to-indigo-600 text-white shadow-xl transform scale-105'
                  : 'bg-white text-purple-600 hover:bg-purple-100 shadow-lg'
              }`}
            >
              {btn.label}
            </button>
          ))}
        </div>

        {/* Chart Container */}
        <div className="bg-white rounded-2xl shadow-2xl p-8 mb-8">
          <h2 className="text-3xl font-bold text-center text-gray-800 mb-6">
            {activeChart === 'comparison' && 'National Food Category Comparison'}
            {activeChart === 'marketShare' && 'Market Share Distribution by Food Type'}
            {activeChart === 'stateWinners' && 'Which Food Wins in Each State?'}
            {activeChart === 'topStates' && 'Top 10 States - Food Breakdown'}
            {activeChart === 'nasiVsRoti' && 'Head-to-Head: Nasi Lemak vs Roti Canai'}
          </h2>

          <ResponsiveContainer width="100%" height={500}>
            {activeChart === 'comparison' && (
              <BarChart data={nationalTotals} layout="vertical">
                <CartesianGrid strokeDasharray="3 3" />
                <XAxis type="number" />
                <YAxis dataKey="name" type="category" width={120} />
                <Tooltip content={<CustomTooltip />} />
                <Bar dataKey="value" name="Monthly Volume (k)">
                  {nationalTotals.map((entry, index) => (
                    <Cell key={`cell-${index}`} fill={entry.color} />
                  ))}
                </Bar>
              </BarChart>
            )}

            {activeChart === 'marketShare' && (
              <PieChart>
                <Pie
                  data={nationalTotals}
                  cx="50%"
                  cy="50%"
                  labelLine={true}
                  label={({ name, percent }) => `${name} (${(percent * 100).toFixed(1)}%)`}
                  outerRadius={180}
                  dataKey="value"
                >
                  {nationalTotals.map((entry, index) => (
                    <Cell key={`cell-${index}`} fill={entry.color} />
                  ))}
                </Pie>
                <Tooltip />
              </PieChart>
            )}

            {activeChart === 'stateWinners' && (
              <div className="overflow-auto max-h-96">
                <table className="w-full">
                  <thead className="bg-purple-600 text-white sticky top-0">
                    <tr>
                      <th className="p-3 text-left">#</th>
                      <th className="p-3 text-left">State</th>
                      <th className="p-3 text-left">Winner</th>
                      <th className="p-3 text-right">Volume (k)</th>
                    </tr>
                  </thead>
                  <tbody>
                    {stateWinners.map((winner, idx) => (
                      <tr key={idx} className={idx % 2 === 0 ? 'bg-gray-50' : 'bg-white'}>
                        <td className="p-3">{idx + 1}</td>
                        <td className="p-3 font-semibold">{winner.state}</td>
                        <td className="p-3">
                          <span className={`px-3 py-1 rounded-full text-sm font-bold ${
                            winner.winner === 'Nasi Lemak' ? 'bg-red-100 text-red-700' : 
                            winner.winner === 'Roti Canai' ? 'bg-teal-100 text-teal-700' : 
                            'bg-gray-100 text-gray-700'
                          }`}>
                            {winner.winner}
                          </span>
                        </td>
                        <td className="p-3 text-right">{winner.value.toLocaleString()}</td>
                      </tr>
                    ))}
                  </tbody>
                </table>
              </div>
            )}

            {activeChart === 'topStates' && (
              <BarChart data={top10States} layout="vertical">
                <CartesianGrid strokeDasharray="3 3" />
                <XAxis type="number" />
                <YAxis dataKey="state" type="category" width={150} />
                <Tooltip content={<CustomTooltip />} />
                <Legend />
                <Bar dataKey="nasiLemak" stackId="a" fill="#FF6B6B" name="Nasi Lemak" />
                <Bar dataKey="rotiCanai" stackId="a" fill="#4ECDC4" name="Roti Canai" />
                <Bar dataKey="nasiGoreng" stackId="a" fill="#FFE66D" name="Nasi Goreng" />
                <Bar dataKey="charKueyTeow" stackId="a" fill="#95E1D3" name="Char Kuey Teow" />
                <Bar dataKey="satay" stackId="a" fill="#F38181" name="Satay" />
                <Bar dataKey="other" stackId="a" fill="#AA96DA" name="Other" />
              </BarChart>
            )}

            {activeChart === 'nasiVsRoti' && (
              <BarChart data={rawData} layout="vertical">
                <CartesianGrid strokeDasharray="3 3" />
                <XAxis type="number" />
                <YAxis dataKey="state" type="category" width={150} />
                <Tooltip content={<CustomTooltip />} />
                <Legend />
                <Bar dataKey="nasiLemak" fill="#FF6B6B" name="Nasi Lemak" />
                <Bar dataKey="rotiCanai" fill="#4ECDC4" name="Roti Canai" />
              </BarChart>
            )}
          </ResponsiveContainer>
        </div>

        {/* Key Insights */}
        <div className="bg-white rounded-2xl shadow-2xl p-8">
          <h2 className="text-3xl font-bold text-purple-600 mb-6">🔍 Key Insights</h2>
          <ul className="space-y-3">
            {summaryStats.isNasiLemakNumber1 ? (
              <>
                <li className="text-lg text-gray-700 border-l-4 border-purple-500 pl-4">
                  📊 Nasi Lemak leads nationally with <strong>{summaryStats.nasiLemakTotal.toLocaleString()}k</strong> monthly volume ({summaryStats.nasiLemakShare}% market share)
                </li>
                <li className="text-lg text-gray-700 border-l-4 border-purple-500 pl-4">
                  🗺️ Nasi Lemak wins in <strong>{summaryStats.nasiLemakWins} out of {summaryStats.totalStates}</strong> states
                </li>
                <li className="text-lg text-gray-700 border-l-4 border-purple-500 pl-4">
                  📈 Lead margin over Roti Canai: <strong>{summaryStats.gapPercentage}%</strong> ({summaryStats.gap.toLocaleString()}k units)
                </li>
              </>
            ) : (
              <>
                <li className="text-lg text-gray-700 border-l-4 border-red-500 pl-4">
                  📊 Roti Canai leads nationally with <strong>{summaryStats.rotiCanaiTotal.toLocaleString()}k</strong> monthly volume
                </li>
                <li className="text-lg text-gray-700 border-l-4 border-red-500 pl-4">
                  📉 Nasi Lemak is 2nd place with <strong>{summaryStats.nasiLemakTotal.toLocaleString()}k</strong> monthly volume
                </li>
                <li className="text-lg text-gray-700 border-l-4 border-red-500 pl-4">
                  📊 Gap: <strong>{Math.abs(summaryStats.gap).toLocaleString()}k</strong> units behind
                </li>
              </>
            )}
            <li className="text-lg text-gray-700 border-l-4 border-blue-500 pl-4">
              🏆 States where Roti Canai wins: <strong>{stateWinners.filter(w => w.winner === 'Roti Canai').map(w => w.state).join(', ') || 'None'}</strong>
            </li>
            <li className="text-lg text-gray-700 border-l-4 border-green-500 pl-4">
              🎯 Closest competition: <strong>{stateWinners.reduce((min, w) => Math.abs(w.gap) < Math.abs(min.gap) ? w : min).state}</strong>
            </li>
          </ul>
        </div>
      </div>
    </div>
  );
};

export default FoodAnalysisDashboard;
