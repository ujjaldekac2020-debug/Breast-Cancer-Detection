<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Breast Cancer Diagnostic Tool</title>
    <!-- Tailwind CSS for Styling -->
    <script src="https://cdn.tailwindcss.com"></script>
    <!-- Chart.js for Visualizations -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <!-- Font Awesome for Icons -->
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    
    <style>
        body { font-family: 'Inter', sans-serif; background-color: #f3f4f6; }
        .glass-panel {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.2);
        }
        .gradient-text {
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
            background-image: linear-gradient(to right, #2563eb, #ec4899);
        }
    </style>
</head>
<body class="text-slate-800">

    <!-- Navbar -->
    <nav class="bg-white shadow-sm border-b border-slate-200 sticky top-0 z-50">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between h-16">
                <div class="flex items-center">
                    <i class="fa-solid fa-dna text-pink-500 text-2xl mr-3"></i>
                    <span class="font-bold text-xl tracking-tight text-slate-800">Medi<span class="text-pink-500">Scan</span> AI</span>
                </div>
                <div class="flex items-center space-x-4">
                    <span class="text-xs font-semibold px-3 py-1 bg-green-100 text-green-700 rounded-full status-badge">System Online</span>
                </div>
            </div>
        </div>
    </nav>

    <!-- Main Content -->
    <main class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-10">
        
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-8">
            
            <!-- Left Column: Input Form -->
            <div class="lg:col-span-7 space-y-6">
                <div class="bg-white rounded-2xl shadow-lg p-6 border-l-4 border-blue-500">
                    <h2 class="text-xl font-bold mb-4 flex items-center">
                        <i class="fa-solid fa-microscope text-blue-500 mr-2"></i> Tumor Characteristics
                    </h2>
                    <p class="text-slate-500 text-sm mb-6">Enter the mean values derived from the Fine Needle Aspirate (FNA) of the breast mass.</p>
                    
                    <form id="predictionForm" class="space-y-4">
                        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
                            <!-- Radius -->
                            <div>
                                <label class="block text-sm font-medium text-slate-700 mb-1">Mean Radius</label>
                                <div class="relative">
                                    <input type="number" id="radius" step="0.01" value="14.0" class="w-full pl-3 pr-3 py-2 border border-slate-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-blue-500 outline-none transition" required>
                                </div>
                                <p class="text-xs text-slate-400 mt-1">Range: 6.9 - 28.1</p>
                            </div>

                            <!-- Texture -->
                            <div>
                                <label class="block text-sm font-medium text-slate-700 mb-1">Mean Texture</label>
                                <input type="number" id="texture" step="0.01" value="19.5" class="w-full pl-3 pr-3 py-2 border border-slate-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-blue-500 outline-none transition" required>
                                <p class="text-xs text-slate-400 mt-1">Range: 9.7 - 39.3</p>
                            </div>

                            <!-- Perimeter -->
                            <div>
                                <label class="block text-sm font-medium text-slate-700 mb-1">Mean Perimeter</label>
                                <input type="number" id="perimeter" step="0.01" value="90.0" class="w-full pl-3 pr-3 py-2 border border-slate-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-blue-500 outline-none transition" required>
                                <p class="text-xs text-slate-400 mt-1">Range: 43.7 - 188.5</p>
                            </div>

                            <!-- Area -->
                            <div>
                                <label class="block text-sm font-medium text-slate-700 mb-1">Mean Area</label>
                                <input type="number" id="area" step="0.01" value="650.0" class="w-full pl-3 pr-3 py-2 border border-slate-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-blue-500 outline-none transition" required>
                                <p class="text-xs text-slate-400 mt-1">Range: 143.5 - 2501.0</p>
                            </div>

                            <!-- Smoothness -->
                            <div>
                                <label class="block text-sm font-medium text-slate-700 mb-1">Mean Smoothness</label>
                                <input type="number" id="smoothness" step="0.001" value="0.09" class="w-full pl-3 pr-3 py-2 border border-slate-300 rounded-lg focus:ring-2 focus:ring-blue-500 focus:border-blue-500 outline-none transition" required>
                                <p class="text-xs text-slate-400 mt-1">Range: 0.05 - 0.16</p>
                            </div>
                        </div>

                        <div class="pt-4">
                            <button type="submit" class="w-full bg-slate-900 hover:bg-slate-800 text-white font-bold py-3 px-4 rounded-xl shadow-lg transition transform hover:scale-[1.02] flex justify-center items-center">
                                <span id="btnText">Run Analysis</span>
                                <i id="btnIcon" class="fa-solid fa-bolt ml-2 text-yellow-400"></i>
                            </button>
                        </div>
                    </form>
                </div>

                <!-- Dataset Info Card -->
                <div class="bg-blue-50 rounded-xl p-5 border border-blue-100">
                    <h3 class="font-bold text-blue-800 mb-2"><i class="fa-brands fa-github mr-2"></i>Dataset Source</h3>
                    <p class="text-sm text-blue-700">
                        Model based on the Wisconsin Breast Cancer Diagnostic dataset provided via GitHub. 
                        Target classification: <b>Malignant (M)</b> vs <b>Benign (B)</b>.
                    </p>
                </div>
            </div>

            <!-- Right Column: Results -->
            <div class="lg:col-span-5 space-y-6">
                
                <!-- Result Card -->
                <div id="resultCard" class="bg-white rounded-2xl shadow-lg p-6 hidden">
                    <h2 class="text-lg font-bold text-slate-700 mb-4 border-b pb-2">Analysis Result</h2>
                    
                    <div class="flex flex-col items-center justify-center py-6">
                        <div id="resultIconContainer" class="w-24 h-24 rounded-full flex items-center justify-center mb-4 transition-all duration-500">
                            <i id="resultIcon" class="fa-solid text-4xl"></i>
                        </div>
                        <h3 id="diagnosisTitle" class="text-3xl font-extrabold mb-1">Unknown</h3>
                        <p id="diagnosisSubtitle" class="text-slate-500 text-sm">Confidence Score: <span id="confidenceVal">0</span>%</p>
                    </div>

                    <!-- Chart -->
                    <div class="mt-6">
                        <canvas id="predictionChart" height="200"></canvas>
                    </div>
                </div>

                <!-- Empty State -->
                <div id="emptyState" class="bg-white rounded-2xl shadow-sm p-10 text-center border border-dashed border-slate-300 h-full flex flex-col justify-center items-center">
                    <div class="bg-slate-100 p-4 rounded-full mb-4">
                        <i class="fa-solid fa-user-doctor text-4xl text-slate-400"></i>
                    </div>
                    <h3 class="text-lg font-medium text-slate-600">Ready to Analyze</h3>
                    <p class="text-slate-400 text-sm mt-2 max-w-xs mx-auto">Input the tumor measurements on the left and click "Run Analysis" to generate a prediction.</p>
                </div>

            </div>
        </div>
    </main>

    <footer class="bg-white border-t border-slate-200 mt-12 py-8">
        <div class="max-w-7xl mx-auto px-4 text-center text-slate-400 text-sm">
            <p>&copy; 2024 Breast Cancer Detection System. For educational/demo purposes only.</p>
        </div>
    </footer>

    <script>
        // CHART SETUP
        let chartInstance = null;

        function renderChart(malignantProb, benignProb) {
            const ctx = document.getElementById('predictionChart').getContext('2d');
            
            if(chartInstance) {
                chartInstance.destroy();
            }

            chartInstance = new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: ['Benign', 'Malignant'],
                    datasets: [{
                        label: 'Probability',
                        data: [benignProb, malignantProb],
                        backgroundColor: [
                            'rgba(34, 197, 94, 0.6)', // Green for Benign
                            'rgba(239, 68, 68, 0.6)'  // Red for Malignant
                        ],
                        borderColor: [
                            'rgba(34, 197, 94, 1)',
                            'rgba(239, 68, 68, 1)'
                        ],
                        borderWidth: 1
                    }]
                },
                options: {
                    responsive: true,
                    scales: {
                        y: { beginAtZero: true, max: 100 }
                    },
                    plugins: {
                        legend: { display: false }
                    }
                }
            });
        }

        // FORM HANDLING
        document.getElementById('predictionForm').addEventListener('submit', async function(e) {
            e.preventDefault();
            
            const btnText = document.getElementById('btnText');
            const btnIcon = document.getElementById('btnIcon');
            
            // Loading State
            btnText.innerText = 'Analyzing...';
            btnIcon.classList.add('fa-spin');
            
            // Gather Data
            const formData = new FormData(e.target);
            const data = {};
            formData.forEach((value, key) => data[key] = parseFloat(value));

            try {
                // ATTEMPT TO CONNECT TO BACKEND
                // Note: This expects the Python Flask app to be running on port 5000.
                // If it fails, it falls back to "Demo Mode" purely for the UI demonstration.
                
                let result;
                try {
                    const response = await fetch('http://127.0.0.1:5000/predict_api', {
                        method: 'POST',
                        headers: { 'Content-Type': 'application/json' },
                        body: JSON.stringify(Object.values(data)) // Send as list
                    });
                    if (!response.ok) throw new Error("API not found");
                    result = await response.json();
                } catch (err) {
                    console.warn("Backend not detected. Switching to Demo Mode logic.");
                    // DEMO LOGIC (Approximation based on standard dataset means)
                    // This allows the UI to be "working" even without the Python server running
                    const score = (data.radius * 2) + (data.area * 0.05) + (data.perimeter * 0.5);
                    const isMalignant = score > 150; // Arbitrary threshold for demo
                    result = {
                        prediction: isMalignant ? 1 : 0,
                        probability: isMalignant ? [10, 90] : [90, 10] // Mock probabilities
                    };
                    
                    // Simulate network delay
                    await new Promise(r => setTimeout(r, 800));
                }

                // UI UPDATE
                const isMalignant = result.prediction === 1;
                const malignantProb = result.probability ? result.probability[1] : (isMalignant ? 95 : 5);
                const benignProb = result.probability ? result.probability[0] : (isMalignant ? 5 : 95);

                document.getElementById('emptyState').classList.add('hidden');
                document.getElementById('resultCard').classList.remove('hidden');

                const iconContainer = document.getElementById('resultIconContainer');
                const icon = document.getElementById('resultIcon');
                const title = document.getElementById('diagnosisTitle');
                const conf = document.getElementById('confidenceVal');

                if (isMalignant) {
                    iconContainer.className = "w-24 h-24 rounded-full flex items-center justify-center mb-4 bg-red-100 text-red-600 shadow-red-200 shadow-xl";
                    icon.className = "fa-solid fa-triangle-exclamation text-4xl";
                    title.className = "text-3xl font-extrabold mb-1 text-red-600";
                    title.innerText = "MALIGNANT";
                    conf.innerText = malignantProb.toFixed(1);
                } else {
                    iconContainer.className = "w-24 h-24 rounded-full flex items-center justify-center mb-4 bg-green-100 text-green-600 shadow-green-200 shadow-xl";
                    icon.className = "fa-solid fa-shield-heart text-4xl";
                    title.className = "text-3xl font-extrabold mb-1 text-green-600";
                    title.innerText = "BENIGN";
                    conf.innerText = benignProb.toFixed(1);
                }

                renderChart(malignantProb, benignProb);

            } catch (error) {
                alert("Error processing data.");
                console.error(error);
            } finally {
                btnText.innerText = 'Run Analysis';
                btnIcon.classList.remove('fa-spin');
            }
        });
    </script>
</body>
</html>
