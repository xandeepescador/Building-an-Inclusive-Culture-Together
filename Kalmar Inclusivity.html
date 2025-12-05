<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Inclusivity Workshop: The Journey to Advocacy</title>
    
    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>
    
    <!-- Chart.js -->
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    
    <!-- Plotly.js -->
    <script src="https://cdn.plot.ly/plotly-2.27.0.min.js"></script>

    <!-- Google Fonts: Inter for clean UI -->
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">

    <!-- Chosen Palette: Warm Neutrals & Earth Tones -->
    <!-- Application Structure Plan: 
         The app is designed as a "Workshop Companion" SPA.
         1. Sidebar Navigation: persistent access to the 3 main views (Overview, Active Session, Advocate Session).
         2. Overview (Home): Contextualizes where the user is in the 4-step journey. Visualizes the shift in mindset.
         3. Session 3 (Active): Uses a "Toolkit" metaphor. Restructured to 2 rows: Top for Coaching (LLM + Checklist), Bottom for Communication (Chart + Micro-Habit Card).
         4. Session 4 (Advocate): Uses a "Dashboard" metaphor. Restructured to 2 rows: Top for Data (Radar Chart + Plotly Matrix), Bottom for Strategy (LLM Metrics + Policy Card).
         This structure moves the user from "Understanding" -> "Practicing" -> "Measuring," mirroring the workshop curriculum.
    -->

    <!-- Visualization & Content Choices:
         1. Maturity Funnel (Chart.js Bar): Visualizes the attrition/progression through the 4 stages (Unaware to Advocate) to set the stage.
         2. Communication Donut (Chart.js): Breaks down the "Inclusive Communication" topic into percentages to show that words are only part of the equation.
         3. Leadership Radar (Chart.js): Used for Session 4 to visualize "Accountability Metrics" across different organizational verticals (Hiring, Retention, etc.), allowing users to see gaps.
         4. Action Project Matrix (Plotly Scatter): Plots projects by "Effort vs. Impact" to help Advocates prioritize systemic changes.
         5. Dynamic Checklist (Vanilla JS): Interactive DOM manipulation for the "One-on-One" guide to make the learning active.
         6. LLM Integration (Gemini API): Two new tools for Session 3 (Coaching Draft) and Session 4 (Metrics Designer).
    -->

    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->

    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #fafaf9; /* stone-50 */
            color: #44403c; /* stone-700 */
        }
        
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 100%; 
            height: 300px; 
            max-height: 400px;
            margin-left: auto;
            margin-right: auto;
        }

        @media (min-width: 768px) {
            .chart-container {
                height: 350px;
            }
        }

        ::-webkit-scrollbar {
            width: 8px;
        }
        ::-webkit-scrollbar-track {
            background: #f5f5f4; 
        }
        ::-webkit-scrollbar-thumb {
            background: #d6d3d1; 
            border-radius: 4px;
        }
        ::-webkit-scrollbar-thumb:hover {
            background: #a8a29e; 
        }

        .nav-item.active {
            background-color: #e7e5e4; /* stone-200 */
            border-right: 4px solid #78716c; /* stone-500 */
            font-weight: 600;
        }

        .fade-in {
            animation: fadeIn 0.4s ease-in-out;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
    </style>
</head>
<body class="flex h-screen overflow-hidden">

    <!-- Sidebar Navigation -->
    <aside class="w-64 bg-stone-100 border-r border-stone-200 flex-shrink-0 hidden md:flex flex-col justify-between">
        <div>
            <div class="p-6 border-b border-stone-200">
                <h1 class="text-xl font-bold text-stone-800 tracking-tight">Inclusion<br>Workshop</h1>
                <p class="text-xs text-stone-500 mt-2 uppercase tracking-widest">Sessions 3 & 4</p>
            </div>
            <nav class="mt-6 flex flex-col gap-1">
                <button onclick="router('overview')" id="nav-overview" class="nav-item w-full text-left px-6 py-3 text-stone-600 hover:bg-stone-200 transition-colors">
                    Overview: The Journey
                </button>
                <button onclick="router('session3')" id="nav-session3" class="nav-item w-full text-left px-6 py-3 text-stone-600 hover:bg-stone-200 transition-colors">
                    Session 3: Active
                </button>
                <button onclick="router('session4')" id="nav-session4" class="nav-item w-full text-left px-6 py-3 text-stone-600 hover:bg-stone-200 transition-colors">
                    Session 4: Advocate
                </button>
            </nav>
        </div>
        <div class="p-6 bg-stone-200 m-4 rounded-lg">
            <h3 class="font-bold text-sm text-stone-700">Next Workshop</h3>
            <p class="text-xs text-stone-500 mt-1">Friday, Oct 24th</p>
            <div class="mt-3 w-full bg-stone-300 h-2 rounded-full overflow-hidden">
                <div class="bg-stone-600 h-full" style="width: 75%"></div>
            </div>
            <p class="text-xs text-stone-500 mt-1 text-right">75% Complete</p>
        </div>
    </aside>

    <!-- Mobile Header -->
    <div class="md:hidden fixed top-0 w-full bg-stone-100 border-b border-stone-200 z-50 flex justify-between items-center p-4">
        <h1 class="font-bold text-stone-800">Inclusion Workshop</h1>
        <button onclick="toggleMobileMenu()" class="text-stone-600 focus:outline-none">
            &#9776;
        </button>
    </div>

    <!-- Mobile Menu Overlay -->
    <div id="mobile-menu" class="fixed inset-0 bg-stone-900 bg-opacity-90 z-40 hidden flex flex-col items-center justify-center space-y-6">
        <button onclick="router('overview'); toggleMobileMenu()" class="text-white text-xl font-medium">Overview</button>
        <button onclick="router('session3'); toggleMobileMenu()" class="text-white text-xl font-medium">Session 3: Active</button>
        <button onclick="router('session4'); toggleMobileMenu()" class="text-white text-xl font-medium">Session 4: Advocate</button>
        <button onclick="toggleMobileMenu()" class="text-stone-400 mt-8">Close</button>
    </div>

    <!-- Main Content Area -->
    <main class="flex-1 overflow-y-auto p-4 md:p-8 pt-20 md:pt-8 bg-stone-50 scroll-smooth" id="main-content">
        
    </main>

    <script>
        const appData = {
            overview: {
                title: "The Path to Systemic Change",
                intro: "Welcome to the advanced modules of our Inclusivity Workshop series. While Sessions 1 and 2 focused on self-reflection and awareness ('Diversity isn't my job' -> 'I see my role'), Sessions 3 and 4 challenge you to take tangible action. This digital companion is designed to help you transition from a passive observer to an active architect of an inclusive culture.",
                stages: [
                    { name: "Unaware", desc: "Diversity isn't my job", count: 15 },
                    { name: "Aware", desc: "I see my role in this", count: 45 },
                    { name: "Active", desc: "I'm ready to step in", count: 30 },
                    { name: "Advocate", desc: "I drive systemic change", count: 10 }
                ]
            },
            session3: {
                title: "Session 3: The Active Mindset",
                intro: "The 'Active' mindset is about breaking inertia. It moves beyond understanding bias to interrupting it in real-time. In this section, explore the 'Manager's Toolkit' for equitable one-on-ones, analyze the components of inclusive communication, and learn how to build micro-habits that foster psychological safety in hybrid environments.",
                checklistItems: [
                    { id: 1, text: "Check bias before the meeting: Am I making assumptions about their workload?", category: "Preparation" },
                    { id: 2, text: "Rotate meeting times to accommodate different time zones/shifts.", category: "Logistics" },
                    { id: 3, text: "Start with 'How are you?' and actually listen to the answer.", category: "Connection" },
                    { id: 4, text: "Ask: 'What barriers are you facing that I can help remove?'", category: "Support" },
                    { id: 5, text: "Solicit feedback: 'How can I support you better next week?'", category: "Growth" }
                ],
                commStats: [30, 20, 40, 10]
            },
            session4: {
                title: "Session 4: The Advocate Mindset",
                intro: "Advocacy is about accountability and systems. It transforms personal conviction into organizational policy. This dashboard allows you to audit your organization's performance, visualize the impact of potential 'Action Learning Projects,' and use data to sustain inclusion efforts beyond this workshop.",
                radarData: {
                    labels: ['Hiring Diversity', 'Pay Equity', 'Promotion Rates', 'Retention', 'Psych Safety Score', 'Access to Training'],
                    current: [65, 70, 40, 55, 60, 50],
                    target: [85, 90, 80, 85, 90, 85]
                },
                projects: [
                    { name: "Mentorship Program", effort: 6, impact: 8, type: "People" },
                    { name: "Blind Resume Review", effort: 4, impact: 7, type: "Process" },
                    { name: "Cultural Holiday Float", effort: 2, impact: 5, type: "Policy" },
                    { name: "ERGs Funding", effort: 5, impact: 6, type: "Community" },
                    { name: "Comp Audit", effort: 8, impact: 9, type: "Structural" }
                ]
            }
        };

        let currentState = {
            view: 'overview',
            checklist: []
        };

        async function callGeminiApi(payload) {
            const apiKey = "";
            const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;
            const maxRetries = 5;

            for (let i = 0; i < maxRetries; i++) {
                try {
                    const response = await fetch(apiUrl, {
                        method: 'POST',
                        headers: { 'Content-Type': 'application/json' },
                        body: JSON.stringify(payload)
                    });

                    if (response.status === 429 && i < maxRetries - 1) {
                        const delay = Math.pow(2, i) * 1000 + Math.random() * 1000;
                        await new Promise(resolve => setTimeout(resolve, delay));
                        continue;
                    }

                    if (!response.ok) {
                        const error = await response.json();
                        throw new Error(error.error.message || `API Error: ${response.status}`);
                    }

                    const result = await response.json();
                    const text = result.candidates?.[0]?.content?.parts?.[0]?.text;
                    if (!text) throw new Error("API response text is empty.");

                    return text;

                } catch (error) {
                    if (i === maxRetries - 1) throw error;
                }
            }
        }

        async function generateInclusiveFeedback() {
            const input = document.getElementById('feedbackInput').value.trim();
            const output = document.getElementById('feedbackOutput');
            const statusDiv = document.getElementById('feedbackStatus');
            const button = document.getElementById('feedbackBtn');

            if (input.length < 20) {
                statusDiv.textContent = "Please describe the situation in more detail (min 20 characters).";
                statusDiv.classList.remove('hidden');
                return;
            }

            button.disabled = true;
            button.innerHTML = '<span class="animate-spin mr-2">&#9696;</span> Drafting...';
            output.innerHTML = '';
            statusDiv.classList.add('hidden');

            try {
                const systemPrompt = "You are an expert Inclusive Coaching specialist. Your task is to take a raw description of a challenging management scenario (e.g., missed deadline, low engagement) and rewrite it into a psychologically safe, constructive, and inclusive coaching opening statement. Focus on separating the person from the problem, maintaining dignity, and focusing on growth and systemic barriers rather than personal failure. Output only the rephrased coaching statement, formatted nicely.";
                
                const userQuery = `Original situation: "${input}"`;

                const payload = {
                    contents: [{ parts: [{ text: userQuery }] }],
                    systemInstruction: { parts: [{ text: systemPrompt }] },
                };

                const result = await callGeminiApi(payload);
                output.textContent = result;
                output.classList.add('font-medium');

            } catch (error) {
                console.error("Gemini API Error:", error);
                output.innerHTML = `<p class="text-red-600">Error generating feedback. Please try again. (${error.message})</p>`;
                output.classList.remove('font-medium');
            } finally {
                button.disabled = false;
                button.innerHTML = '✨ Generate Inclusive Feedback';
            }
        }

        async function defineAccountabilityMetrics() {
            const input = document.getElementById('alpInput').value.trim();
            const output = document.getElementById('alpOutput');
            const statusDiv = document.getElementById('alpStatus');
            const button = document.getElementById('alpBtn');

            if (input.length < 10) {
                statusDiv.textContent = "Please input a clear Action Learning Project goal (min 10 characters).";
                statusDiv.classList.remove('hidden');
                return;
            }

            button.disabled = true;
            button.innerHTML = '<span class="animate-spin mr-2">&#9696;</span> Analyzing Goal...';
            output.innerHTML = '';
            statusDiv.classList.add('hidden');

            try {
                const systemPrompt = "You are a specialist in DEI Accountability and Metrics. The user will provide an Action Learning Project (ALP) goal. Your task is to generate 3 to 5 highly specific, measurable, achievable, relevant, and time-bound (SMART) Key Performance Indicators (KPIs) for this project, focusing on systemic inclusion change. Format the output as a clean, bulleted list of KPIs.";
                
                const userQuery = `Action Learning Project Goal: "${input}"`;

                const payload = {
                    contents: [{ parts: [{ text: userQuery }] }],
                    systemInstruction: { parts: [{ text: systemPrompt }] },
                };

                const result = await callGeminiApi(payload);
                output.innerHTML = result;
                output.classList.add('font-medium');

            } catch (error) {
                console.error("Gemini API Error:", error);
                output.innerHTML = `<p class="text-red-600">Error generating metrics. Please try again. (${error.message})</p>`;
                output.classList.remove('font-medium');
            } finally {
                button.disabled = false;
                button.innerHTML = '✨ Define Accountability Metrics';
            }
        }

        function router(viewName) {
            currentState.view = viewName;
            
            document.querySelectorAll('.nav-item').forEach(el => el.classList.remove('active'));
            const activeNav = document.getElementById(`nav-${viewName}`);
            if(activeNav) activeNav.classList.add('active');

            const main = document.getElementById('main-content');
            main.innerHTML = '';
            
            main.scrollTop = 0;

            if (viewName === 'overview') renderOverview();
            else if (viewName === 'session3') renderSession3();
            else if (viewName === 'session4') renderSession4();
        }

        function toggleMobileMenu() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        }

        function renderOverview() {
            const main = document.getElementById('main-content');
            const data = appData.overview;

            main.innerHTML = `
                <div class="fade-in max-w-5xl mx-auto">
                    <header class="mb-8">
                        <h2 class="text-3xl font-bold text-stone-800 mb-4">${data.title}</h2>
                        <p class="text-lg text-stone-600 leading-relaxed">${data.intro}</p>
                    </header>

                    <div class="grid grid-cols-1 lg:grid-cols-3 gap-6 mb-8">
                        <div class="bg-white p-6 rounded-xl shadow-sm border border-stone-200 lg:col-span-2">
                            <h3 class="font-bold text-stone-700 mb-2">The Inclusion Maturity Model</h3>
                            <p class="text-sm text-stone-500 mb-6">Current breakdown of organizational mindset. Goal: Shift right.</p>
                            <div class="chart-container">
                                <canvas id="maturityChart"></canvas>
                            </div>
                        </div>

                        <div class="bg-stone-100 p-6 rounded-xl border border-stone-200 flex flex-col justify-center space-y-4">
                            <h3 class="font-bold text-stone-700 border-b border-stone-300 pb-2">Quick Recall</h3>
                            <div>
                                <h4 class="font-semibold text-stone-800 text-sm">Bias (Session 1)</h4>
                                <p class="text-xs text-stone-600">Prejudice in favor of or against one thing, person, or group compared with another.</p>
                            </div>
                            <div>
                                <h4 class="font-semibold text-stone-800 text-sm">Inclusive Leadership (Session 2)</h4>
                                <p class="text-xs text-stone-600">The ability to lead a diverse group of people while ensuring they feel respected and valued.</p>
                            </div>
                            <div class="pt-4">
                                <button onclick="router('session3')" class="w-full bg-stone-700 text-white py-2 px-4 rounded hover:bg-stone-800 transition shadow">
                                    Start Session 3 &rarr;
                                </button>
                            </div>
                        </div>
                    </div>

                    <div class="bg-white p-6 rounded-xl shadow-sm border border-stone-200">
                        <h3 class="font-bold text-stone-700 mb-4">Workshop Timeline</h3>
                        <div class="flex flex-col md:flex-row justify-between items-center relative">
                            <div class="absolute top-1/2 left-0 w-full h-1 bg-stone-200 -z-10 hidden md:block"></div>
                            
                            <div class="flex flex-col items-center bg-white p-2 z-10 opacity-50">
                                <div class="w-8 h-8 rounded-full bg-stone-300 flex items-center justify-center text-white font-bold mb-2">1</div>
                                <span class="text-xs font-bold text-stone-400">Unaware</span>
                            </div>
                            <div class="flex flex-col items-center bg-white p-2 z-10 opacity-50">
                                <div class="w-8 h-8 rounded-full bg-stone-300 flex items-center justify-center text-white font-bold mb-2">2</div>
                                <span class="text-xs font-bold text-stone-400">Aware</span>
                            </div>
                            <div class="flex flex-col items-center bg-white p-2 z-10">
                                <div class="w-10 h-10 rounded-full bg-stone-600 flex items-center justify-center text-white font-bold mb-2 ring-4 ring-stone-100">3</div>
                                <span class="text-sm font-bold text-stone-700">Active</span>
                            </div>
                            <div class="flex flex-col items-center bg-white p-2 z-10">
                                <div class="w-10 h-10 rounded-full bg-stone-600 flex items-center justify-center text-white font-bold mb-2 ring-4 ring-stone-100">4</div>
                                <span class="text-sm font-bold text-stone-700">Advocate</span>
                            </div>
                        </div>
                    </div>
                </div>
            `;

            setTimeout(() => {
                const ctx = document.getElementById('maturityChart').getContext('2d');
                new Chart(ctx, {
                    type: 'bar',
                    data: {
                        labels: data.stages.map(s => s.name),
                        datasets: [{
                            label: '% of Organization',
                            data: data.stages.map(s => s.count),
                            backgroundColor: ['#d6d3d1', '#a8a29e', '#57534e', '#292524'],
                            borderRadius: 6
                        }]
                    },
                    options: {
                        responsive: true,
                        maintainAspectRatio: false,
                        plugins: {
                            legend: { display: false },
                            tooltip: {
                                callbacks: {
                                    afterLabel: function(context) {
                                        return data.stages[context.dataIndex].desc;
                                    }
                                }
                            }
                        },
                        scales: {
                            y: { beginAtZero: true, grid: { color: '#f5f5f4' } },
                            x: { grid: { display: false } }
                        }
                    }
                });
            }, 100);
        }

        function renderSession3() {
            const main = document.getElementById('main-content');
            const data = appData.session3;

            main.innerHTML = `
                <div class="fade-in max-w-6xl mx-auto">
                    <header class="mb-8 border-b border-stone-200 pb-6">
                        <div class="flex items-center gap-2 mb-2">
                            <span class="bg-stone-200 text-stone-700 text-xs px-2 py-1 rounded font-bold uppercase">Session Three</span>
                            <span class="text-stone-400 text-xs">Mindset: "I'm ready to step in"</span>
                        </div>
                        <h2 class="text-3xl font-bold text-stone-800 mb-4">Active Leadership & Coaching</h2>
                        <p class="text-stone-600 max-w-3xl">${data.intro}</p>
                    </header>

                    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                        
                        <!-- New LLM Feature: Coaching Draft -->
                        <div class="bg-white rounded-xl shadow-sm border border-stone-200 overflow-hidden flex flex-col">
                            <div class="p-6 bg-stone-100 border-b border-stone-200">
                                <h3 class="font-bold text-lg text-stone-800 flex items-center gap-2">
                                    ✨ Inclusive Coaching Draft
                                </h3>
                                <p class="text-sm text-stone-500 mt-1">Input a challenging situation (e.g., missed deadline) to receive psychologically safe coaching language.</p>
                            </div>
                            <div class="p-6 flex-1 space-y-4">
                                <textarea id="feedbackInput" class="w-full p-3 border border-stone-300 rounded focus:ring-stone-500 focus:border-stone-500" rows="4" placeholder="Describe the situation you need to address (e.g., 'A team member delivered a project late and blamed workload')."></textarea>
                                <button onclick="generateInclusiveFeedback()" id="feedbackBtn" class="w-full bg-stone-700 text-white py-2 px-4 rounded hover:bg-stone-800 transition shadow flex items-center justify-center gap-2">
                                    ✨ Generate Inclusive Feedback
                                </button>
                                <div id="feedbackOutput" class="mt-4 p-4 bg-stone-50 rounded border border-stone-200 min-h-[50px] text-sm text-stone-700 whitespace-pre-wrap">
                                    <p class="text-stone-400 italic">Generated feedback will appear here.</p>
                                </div>
                                <div id="feedbackStatus" class="text-sm text-center text-red-600 hidden"></div>
                            </div>
                        </div>

                        <!-- Tool 1: Interactive Checklist -->
                        <div class="bg-white rounded-xl shadow-sm border border-stone-200 overflow-hidden flex flex-col">
                            <div class="p-6 bg-stone-100 border-b border-stone-200">
                                <h3 class="font-bold text-lg text-stone-800">Equitable One-on-One Builder</h3>
                                <p class="text-sm text-stone-500 mt-1">Select items to build your agenda for the next meeting. Focus on removing barriers.</p>
                            </div>
                            <div class="p-6 flex-1">
                                <div id="checklist-container" class="space-y-3">
                                    ${data.checklistItems.map(item => `
                                        <div class="flex items-start gap-3 p-3 rounded hover:bg-stone-50 transition cursor-pointer" onclick="toggleCheck(${item.id})">
                                            <div class="mt-1 w-5 h-5 rounded border border-stone-300 flex items-center justify-center bg-white" id="box-${item.id}">
                                                <span class="text-stone-800 text-xs hidden checkmark">&#10003;</span>
                                            </div>
                                            <div>
                                                <span class="text-xs font-bold text-stone-400 uppercase tracking-wide">${item.category}</span>
                                                <p class="text-stone-700 text-sm">${item.text}</p>
                                            </div>
                                        </div>
                                    `).join('')}
                                </div>
                            </div>
                            <div class="p-4 bg-stone-50 border-t border-stone-200 text-center">
                                <p class="text-xs text-stone-400 italic">"Consistency creates psychological safety."</p>
                            </div>
                        </div>
                    </div>

                    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8 mt-8">
                        <!-- Tool 2: Communication Breakdown -->
                        <div class="bg-white p-6 rounded-xl shadow-sm border border-stone-200">
                            <h3 class="font-bold text-lg text-stone-800 mb-2">Inclusive Communication Mix</h3>
                            <p class="text-sm text-stone-500 mb-4">In hybrid environments, intent does not always equal impact. Where does miscommunication happen?</p>
                            <div class="chart-container">
                                <canvas id="commChart"></canvas>
                            </div>
                        </div>

                        <!-- Micro-habit Card -->
                        <div class="bg-stone-700 text-white p-6 rounded-xl shadow-lg relative overflow-hidden">
                            <div class="relative z-10">
                                <h3 class="font-bold text-xl mb-2">Micro-Habit Challenge</h3>
                                <p class="text-stone-300 text-sm mb-4">"The 2-Minute Pause"</p>
                                <p class="text-sm leading-relaxed mb-4">
                                    Before giving feedback, pause for 2 minutes. Ask yourself: "Am I critiquing the work or the personality? Is this feedback actionable?"
                                </p>
                                <button class="bg-stone-500 hover:bg-stone-400 text-white text-xs py-2 px-4 rounded transition">Accept Challenge</button>
                            </div>
                            <div class="absolute top-0 right-0 -mt-4 -mr-4 text-stone-600 opacity-20 text-9xl font-serif">"</div>
                        </div>
                    </div>
                    
                    <div class="mt-8 flex justify-end">
                         <button onclick="router('session4')" class="flex items-center gap-2 text-stone-600 hover:text-stone-900 font-medium transition">
                            Next: The Advocate Mindset &rarr;
                        </button>
                    </div>
                </div>
            `;

            setTimeout(() => {
                const ctx = document.getElementById('commChart').getContext('2d');
                new Chart(ctx, {
                    type: 'doughnut',
                    data: {
                        labels: ['Tone & Body Language', 'Timing/Context', 'Verbal Content', 'Medium (Slack/Email)'],
                        datasets: [{
                            data: data.commStats,
                            backgroundColor: ['#e7e5e4', '#d6d3d1', '#a8a29e', '#57534e'],
                            borderWidth: 0,
                            hoverOffset: 4
                        }]
                    },
                    options: {
                        responsive: true,
                        maintainAspectRatio: false,
                        plugins: {
                            legend: { position: 'right', labels: { boxWidth: 12, usePointStyle: true } }
                        }
                    }
                });
            }, 100);
        }

        function renderSession4() {
            const main = document.getElementById('main-content');
            const data = appData.session4;

            main.innerHTML = `
                <div class="fade-in max-w-6xl mx-auto">
                    <header class="mb-8 border-b border-stone-200 pb-6">
                        <div class="flex items-center gap-2 mb-2">
                            <span class="bg-stone-800 text-white text-xs px-2 py-1 rounded font-bold uppercase">Session Four</span>
                            <span class="text-stone-400 text-xs">Mindset: "I drive systemic change"</span>
                        </div>
                        <h2 class="text-3xl font-bold text-stone-800 mb-4">Systemic Advocacy & Metrics</h2>
                        <p class="text-stone-600 max-w-3xl">${data.intro}</p>
                    </header>

                    <!-- Top Row: Metrics and Impact Matrix -->
                    <div class="mb-8 grid grid-cols-1 lg:grid-cols-3 gap-6">
                        <div class="lg:col-span-1 bg-white p-6 rounded-xl shadow-sm border border-stone-200">
                            <h3 class="font-bold text-stone-800 mb-2">Inclusion Gap Analysis</h3>
                            <p class="text-xs text-stone-500 mb-4">Comparing current metrics against organizational targets (Year-End Goals).</p>
                            <div class="chart-container">
                                <canvas id="radarChart"></canvas>
                            </div>
                        </div>

                        <div class="lg:col-span-2 bg-white p-6 rounded-xl shadow-sm border border-stone-200 flex flex-col">
                            <h3 class="font-bold text-stone-800 mb-2">Action Learning Projects: Impact Matrix</h3>
                            <p class="text-xs text-stone-500 mb-4">Prioritize initiatives based on Effort (Resources/Time) vs. Impact (Systemic Change). Focus on high-impact, manageable effort (Top Left/Center).</p>
                            <div id="plotlyChart" class="w-full flex-1" style="min-height: 300px;"></div>
                        </div>
                    </div>

                    <!-- Bottom Row: Strategy & Accountability -->
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        
                        <!-- New LLM Feature: ALP Metrics Designer -->
                        <div class="bg-stone-100 p-6 rounded-xl border border-stone-200">
                            <h3 class="font-bold text-stone-800 mb-4 flex items-center gap-2">
                                ✨ ALP Metrics Designer
                            </h3>
                            <p class="text-sm text-stone-500 mb-4">Input an Action Learning Project goal (e.g., 'Launch a neurodiversity hiring pilot') to generate measurable KPIs.</p>
                            
                            <input type="text" id="alpInput" class="w-full p-3 border border-stone-300 rounded focus:ring-stone-500 focus:border-stone-500 mb-3" placeholder="Project Goal (e.g., Improve promotion equity)">
                            <button onclick="defineAccountabilityMetrics()" id="alpBtn" class="w-full bg-stone-700 text-white py-2 px-4 rounded hover:bg-stone-800 transition shadow flex items-center justify-center gap-2">
                                ✨ Define Accountability Metrics
                            </button>

                            <div id="alpOutput" class="mt-4 p-4 bg-white rounded border border-stone-200 min-h-[50px] text-sm text-stone-700 whitespace-pre-wrap">
                                <p class="text-stone-400 italic">Generated KPIs (e.g., Increase diverse hires by 15%).</p>
                            </div>
                            <div id="alpStatus" class="text-sm text-center text-red-600 hidden"></div>
                        </div>


                        <div class="bg-stone-800 text-white p-6 rounded-xl shadow-lg">
                            <h3 class="font-bold text-lg mb-4">Performance Management Integration</h3>
                            <p class="text-sm text-stone-300 mb-6">Advocacy means tying inclusion to business results. Ensure your upcoming reviews include:</p>
                            <div class="space-y-2">
                                <div class="flex items-center gap-3">
                                    <span class="text-green-400 font-bold">&check;</span>
                                    <span class="text-sm">Specific examples of inclusive team building.</span>
                                </div>
                                <div class="flex items-center gap-3">
                                    <span class="text-green-400 font-bold">&check;</span>
                                    <span class="text-sm">Metrics on diverse talent retention.</span>
                                </div>
                                <div class="flex items-center gap-3">
                                    <span class="text-green-400 font-bold">&check;</span>
                                    <span class="text-sm">360-feedback on psychological safety.</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            `;

            setTimeout(() => {
                const ctx = document.getElementById('radarChart').getContext('2d');
                new Chart(ctx, {
                    type: 'radar',
                    data: {
                        labels: data.radarData.labels,
                        datasets: [{
                            label: 'Current Status',
                            data: data.radarData.current,
                            fill: true,
                            backgroundColor: 'rgba(168, 162, 158, 0.2)', 
                            borderColor: 'rgb(168, 162, 158)',
                            pointBackgroundColor: 'rgb(168, 162, 158)',
                            pointBorderColor: '#fff',
                            pointHoverBackgroundColor: '#fff',
                            pointHoverBorderColor: 'rgb(168, 162, 158)'
                        }, {
                            label: 'Target Goal',
                            data: data.radarData.target,
                            fill: true,
                            backgroundColor: 'rgba(87, 83, 78, 0.2)', 
                            borderColor: 'rgb(87, 83, 78)',
                            pointBackgroundColor: 'rgb(87, 83, 78)',
                            pointBorderColor: '#fff',
                            pointHoverBackgroundColor: '#fff',
                            pointHoverBorderColor: 'rgb(87, 83, 78)'
                        }]
                    },
                    options: {
                        responsive: true,
                        maintainAspectRatio: false,
                        elements: { line: { borderWidth: 3 } },
                        scales: {
                            r: {
                                angleLines: { display: true },
                                suggestedMin: 0,
                                suggestedMax: 100
                            }
                        },
                        plugins: {
                            legend: { position: 'bottom', labels: { font: { size: 10 } } }
                        }
                    }
                });

                const trace1 = {
                    x: data.projects.map(p => p.effort),
                    y: data.projects.map(p => p.impact),
                    mode: 'markers+text',
                    type: 'scatter',
                    text: data.projects.map(p => p.name),
                    textposition: 'top center',
                    marker: { size: 12, color: '#57534e' },
                    hoverinfo: 'text',
                    hovertext: data.projects.map(p => `Type: ${p.type}<br>Effort: ${p.effort}<br>Impact: ${p.impact}`)
                };

                const layout = {
                    margin: { t: 20, r: 20, b: 40, l: 40 },
                    paper_bgcolor: 'rgba(0,0,0,0)',
                    plot_bgcolor: 'rgba(0,0,0,0)',
                    xaxis: { title: 'Effort Required (1-10)', range: [0, 11], showgrid: true, gridcolor: '#e7e5e4' },
                    yaxis: { title: 'Systemic Impact (1-10)', range: [0, 11], showgrid: true, gridcolor: '#e7e5e4' },
                    shapes: [
                        { type: 'rect', x0: 0, y0: 5, x1: 5, y1: 10, fillcolor: '#e7e5e4', opacity: 0.2, line: { width: 0 } }
                    ],
                    annotations: [
                        { x: 2.5, y: 9.5, xref: 'x', yref: 'y', text: 'Quick Wins', showarrow: false, font: { color: '#78716c' } },
                        { x: 8, y: 9.5, xref: 'x', yref: 'y', text: 'Strategic Bets', showarrow: false, font: { color: '#78716c' } }
                    ]
                };

                Plotly.newPlot('plotlyChart', [trace1], layout, { displayModeBar: false, responsive: true });

            }, 100);
        }

        function toggleCheck(id) {
            const box = document.getElementById(`box-${id}`);
            const check = box.querySelector('.checkmark');
            
            if (check.classList.contains('hidden')) {
                check.classList.remove('hidden');
                box.classList.add('bg-stone-200');
            } else {
                check.classList.add('hidden');
                box.classList.remove('bg-stone-200');
            }
        }

        document.addEventListener('DOMContentLoaded', () => {
            router('overview');
        });

    </script>
</body>
</html>
