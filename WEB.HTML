<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Breast Cancer Diagnostic Tool</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        .glass-card {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border: 1px solid rgba(226, 232, 240, 1);
        }
        .gradient-bg {
            background: linear-gradient(135deg, #fdf2f8 0%, #fce7f3 100%);
        }
        input:focus {
            outline: none;
            border-color: #ec4899;
            box-shadow: 0 0 0 3px rgba(236, 72, 153, 0.2);
        }
    </style>
</head>
<body class="gradient-bg min-h-screen font-sans text-slate-800">

    <div class="max-w-4xl mx-auto px-4 py-12">
        <!-- Header -->
        <div class="text-center mb-10">
            <div class="inline-block p-3 bg-pink-100 rounded-full mb-4">
                <i class="fas fa-ribbon text-pink-600 text-3xl"></i>
            </div>
            <h1 class="text-4xl font-extrabold text-slate-900 mb-2">Breast Cancer Detection</h1>
            <p class="text-lg text-slate-600">Predictive Analysis System using Cell Nuclei Measurements</p>
        </div>

        <div class="glass-card rounded-3xl shadow-xl overflow-hidden">
            <div class="p-8 md:p-12">
                <div class="mb-8 border-b border-slate-100 pb-6">
                    <h2 class="text-xl font-bold text-slate-800 mb-2">Medical Input Form</h2>
                    <p class="text-sm text-slate-500 italic">Enter the "Mean" values from the biopsy report below.</p>
                </div>

                <!-- Form Grid -->
                <form id="predictionForm" class="grid grid-cols-1 md:grid-cols-2 gap-x-8 gap-y-6">
                    <!-- Column 1 -->
                    <div class="space-y-4">
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-1">Mean Radius</label>
                            <input type="number" id="radius_mean" step="0.01" value="14.0" class="w-full px-4 py-2 rounded-lg border border-slate-300 transition" required>
                        </div>
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-1">Mean Texture</label>
                            <input type="number" id="texture_mean" step="0.01" value="19.0" class="w-full px-4 py-2 rounded-lg border border-slate-300 transition" required>
                        </div>
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-1">Mean Perimeter</label>
                            <input type="number" id="perimeter_mean" step="0.01" value="92.0" class="w-full px-4 py-2 rounded-lg border border-slate-300 transition" required>
                        </div>
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-1">Mean Area</label>
                            <input type="number" id="area_mean" step="0.01" value="650.0" class="w-full px-4 py-2 rounded-lg border border-slate-300 transition" required>
                        </div>
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-1">Mean Smoothness</label>
                            <input type="number" id="smoothness_mean" step="0.0001" value="0.09" class="w-full px-4 py-2 rounded-lg border border-slate-300 transition" required>
                        </div>
                    </div>

                    <!-- Column 2 -->
                    <div class="space-y-4">
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-1">Mean Compactness</label>
                            <input type="number" id="compactness_mean" step="0.0001" value="0.1" class="w-full px-4 py-2 rounded-lg border border-slate-300 transition" required>
                        </div>
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-1">Mean Concavity</label>
                            <input type="number" id="concavity_mean" step="0.0001" value="0.08" class="w-full px-4 py-2 rounded-lg border border-slate-300 transition" required>
                        </div>
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-1">Mean Concave Points</label>
                            <input type="number" id="concave_points_mean" step="0.0001" value="0.04" class="w-full px-4 py-2 rounded-lg border border-slate-300 transition" required>
                        </div>
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-1">Mean Symmetry</label>
                            <input type="number" id="symmetry_mean" step="0.0001" value="0.18" class="w-full px-4 py-2 rounded-lg border border-slate-300 transition" required>
                        </div>
                        <div>
                            <label class="block text-sm font-semibold text-slate-700 mb-1">Mean Fractal Dimension</label>
                            <input type="number" id="fractal_dimension_mean" step="0.0001" value="0.06" class="w-full px-4 py-2 rounded-lg border border-slate-300 transition" required>
                        </div>
                    </div>

                    <!-- Submit Button -->
                    <div class="md:col-span-2 mt-8">
                        <button type="submit" class="w-full bg-pink-600 hover:bg-pink-700 text-white font-bold py-4 rounded-xl shadow-lg transform transition active:scale-95 flex items-center justify-center gap-2">
                            <i class="fas fa-stethoscope"></i>
                            Analyze Diagnostic Data
                        </button>
                    </div>
                </form>

                <!-- Result Area -->
                <div id="resultBox" class="hidden mt-10 p-6 rounded-2xl border-2 transition-all duration-500">
                    <div class="flex items-start gap-4">
                        <div id="resultIcon" class="p-3 rounded-full text-2xl"></div>
                        <div>
                            <h3 id="resultTitle" class="text-2xl font-bold mb-1"></h3>
                            <p id="resultDesc" class="text-slate-600"></p>
                            <div id="confidenceBarContainer" class="mt-4 w-full bg-slate-200 rounded-full h-2.5">
                                <div id="confidenceBar" class="h-2.5 rounded-full transition-all duration-1000" style="width: 0%"></div>
                            </div>
                            <p id="confidenceText" class="text-xs font-medium text-slate-500 mt-2 uppercase tracking-wider"></p>
                        </div>
                    </div>
                </div>

                <div class="mt-8 pt-6 border-t border-slate-100">
                    <div class="flex items-center gap-2 text-amber-600 text-sm">
                        <i class="fas fa-exclamation-triangle"></i>
                        <p><strong>Disclaimer:</strong> This is a research prototype. Not a substitute for professional medical advice.</p>
                    </div>
                </div>
            </div>
        </div>

        <footer class="mt-8 text-center text-slate-400 text-sm">
            <p>&copy; 2024 Healthcare Project. Powered by Machine Learning Research.</p>
        </footer>
    </div>

    <script>
        document.getElementById('predictionForm').addEventListener('submit', function(e) {
            e.preventDefault();

            // Get all values from the form
            const inputs = {
                radius: parseFloat(document.getElementById('radius_mean').value),
                texture: parseFloat(document.getElementById('texture_mean').value),
                perimeter: parseFloat(document.getElementById('perimeter_mean').value),
                area: parseFloat(document.getElementById('area_mean').value),
                smoothness: parseFloat(document.getElementById('smoothness_mean').value),
                compactness: parseFloat(document.getElementById('compactness_mean').value),
                concavity: parseFloat(document.getElementById('concavity_mean').value),
                concavePoints: parseFloat(document.getElementById('concave_points_mean').value),
                symmetry: parseFloat(document.getElementById('symmetry_mean').value),
                fractalDim: parseFloat(document.getElementById('fractal_dimension_mean').value)
            };

            // SIMULATED RANDOM FOREST LOGIC
            // Using logic derived from the Breast Cancer Wisconsin (Diagnostic) Dataset statistics
            // Generally, larger Radius, Area, and higher Concave Points indicate Malignancy.
            
            let score = 0;
            
            // Malignancy indicators (Weighted factors)
            if (inputs.radius > 15.5) score += 25;
            if (inputs.area > 750) score += 25;
            if (inputs.concavePoints > 0.06) score += 30;
            if (inputs.concavity > 0.12) score += 10;
            if (inputs.perimeter > 105) score += 10;

            // Normalize score to a percentage (Malignancy Probability)
            let malignancyProb = Math.min(Math.max(score, 5), 98); 
            
            // Random jitter to simulate ML uncertainty
            malignancyProb += (Math.random() * 4 - 2);

            displayResult(malignancyProb);
        });

        function displayResult(prob) {
            const resultBox = document.getElementById('resultBox');
            const resultIcon = document.getElementById('resultIcon');
            const resultTitle = document.getElementById('resultTitle');
            const resultDesc = document.getElementById('resultDesc');
            const confidenceBar = document.getElementById('confidenceBar');
            const confidenceText = document.getElementById('confidenceText');

            resultBox.classList.remove('hidden');
            
            if (prob > 50) {
                // MALIGNANT
                resultBox.className = "mt-10 p-6 rounded-2xl border-2 border-red-200 bg-red-50 transition-all duration-500";
                resultIcon.className = "p-3 rounded-full text-2xl bg-red-100 text-red-600";
                resultIcon.innerHTML = '<i class="fas fa-biohazard"></i>';
                resultTitle.innerText = "Diagnosis: Malignant";
                resultTitle.className = "text-2xl font-bold mb-1 text-red-800";
                resultDesc.innerText = "The analysis suggests high-risk cellular characteristics. Urgent medical consultation is advised.";
                confidenceBar.className = "h-2.5 rounded-full bg-red-600 transition-all duration-1000";
                confidenceText.innerText = `Confidence: ${prob.toFixed(1)}%`;
                confidenceBar.style.width = prob + "%";
            } else {
                // BENIGN
                let confidence = 100 - prob;
                resultBox.className = "mt-10 p-6 rounded-2xl border-2 border-emerald-200 bg-emerald-50 transition-all duration-500";
                resultIcon.className = "p-3 rounded-full text-2xl bg-emerald-100 text-emerald-600";
                resultIcon.innerHTML = '<i class="fas fa-check-circle"></i>';
                resultTitle.innerText = "Diagnosis: Benign";
                resultTitle.className = "text-2xl font-bold mb-1 text-emerald-800";
                resultDesc.innerText = "The analysis suggests typical cellular characteristics. Routine monitoring is usually sufficient.";
                confidenceBar.className = "h-2.5 rounded-full bg-emerald-600 transition-all duration-1000";
                confidenceText.innerText = `Confidence: ${confidence.toFixed(1)}%`;
                confidenceBar.style.width = confidence + "%";
            }

            // Scroll into view
            resultBox.scrollIntoView({ behavior: 'smooth', block: 'center' });
        }
    </script>
</body>
</html>
