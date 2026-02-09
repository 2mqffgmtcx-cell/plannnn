
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Немецкий язык - План подготовки до C1</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 10px;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background: white;
            border-radius: 15px;
            box-shadow: 0 10px 40px rgba(0,0,0,0.3);
            overflow: hidden;
        }
        
        .header {
            position: relative;
            height: 200px;
            overflow: hidden;
        }
        
        .header-image {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }
        
        .header-overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(to bottom, rgba(0,0,0,0.3), rgba(0,0,0,0.8));
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            color: white;
            text-align: center;
            padding: 15px;
        }
        
        .header h1 {
            font-size: 1.8em;
            margin-bottom: 8px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.5);
        }
        
        .header p {
            font-size: 0.95em;
            opacity: 0.9;
            line-height: 1.4;
        }
        
        .days-counter {
            background: rgba(255,255,255,0.25);
            padding: 8px 16px;
            border-radius: 20px;
            margin-top: 10px;
            font-size: 0.9em;
            backdrop-filter: blur(10px);
        }
        
        .content {
            padding: 15px;
        }
        
        .date-nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
            padding: 12px;
            background: #f8f9fa;
            border-radius: 12px;
            gap: 8px;
        }
        
        .date-nav button {
            background: #667eea;
            color: white;
            border: none;
            padding: 10px 14px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 13px;
            font-weight: 600;
            transition: all 0.3s;
            white-space: nowrap;
            min-width: 44px;
            min-height: 44px;
        }
        
        .date-nav button:hover {
            background: #5568d3;
            transform: translateY(-1px);
        }
        
        .current-date {
            font-size: 0.95em;
            font-weight: bold;
            color: #333;
            text-align: center;
            line-height: 1.3;
            flex: 1;
        }
        
        .tasks-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 12px;
            margin-bottom: 20px;
        }
        
        .task-card {
            background: white;
            border-radius: 12px;
            padding: 15px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            border-left: 4px solid #ddd;
            transition: transform 0.2s, box-shadow 0.2s;
        }
        
        .task-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 4px 12px rgba(0,0,0,0.15);
        }
        
        .task-card.completed {
            border-left-color: #28a745;
            background: #f8fff8;
        }
        
        .task-card.partial {
            border-left-color: #ffc107;
            background: #fffbf0;
        }
        
        .task-card.not-started {
            border-left-color: #dc3545;
            background: #fff8f8;
        }
        
        .task-header {
            display: flex;
            justify-content: space-between;
            align-items: flex-start;
            margin-bottom: 10px;
            gap: 8px;
        }
        
        .task-title {
            font-size: 1em;
            font-weight: bold;
            color: #333;
            line-height: 1.3;
            flex: 1;
        }
        
        .task-status {
            padding: 4px 10px;
            border-radius: 15px;
            font-size: 0.75em;
            font-weight: bold;
            white-space: nowrap;
            flex-shrink: 0;
        }
        
        .status-completed {
            background: #d4edda;
            color: #155724;
        }
        
        .status-partial {
            background: #fff3cd;
            color: #856404;
        }
        
        .status-not-started {
            background: #f8d7da;
            color: #721c24;
        }
        
        .task-plan {
            background: #e9ecef;
            padding: 8px 10px;
            border-radius: 6px;
            margin-bottom: 10px;
            font-size: 0.85em;
            line-height: 1.4;
        }
        
        .task-input {
            display: flex;
            gap: 8px;
            align-items: center;
            margin-bottom: 8px;
        }
        
        .task-input input[type="number"] {
            flex: 1;
            padding: 10px;
            border: 2px solid #ddd;
            border-radius: 8px;
            font-size: 16px;
            min-height: 44px;
        }
        
        .task-input button {
            background: #28a745;
            color: white;
            border: none;
            padding: 10px 16px;
            border-radius: 8px;
            cursor: pointer;
            font-size: 14px;
            font-weight: 600;
            min-height: 44px;
            min-width: 44px;
        }
        
        .task-input button:hover {
            background: #218838;
        }
        
        .task-progress {
            margin-top: 10px;
            padding-top: 10px;
            border-top: 1px solid #eee;
        }
        
        .progress-bar {
            height: 8px;
            background: #e9ecef;
            border-radius: 4px;
            overflow: hidden;
            margin-bottom: 6px;
        }
        
        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #667eea, #764ba2);
            transition: width 0.5s ease;
        }
        
        .progress-text {
            font-size: 0.8em;
            color: #666;
            text-align: center;
            line-height: 1.4;
        }
        
        .stats-section {
            background: #f8f9fa;
            padding: 20px 15px;
            border-radius: 12px;
            margin-top: 20px;
        }
        
        .stats-section h2 {
            font-size: 1.1em;
            margin-bottom: 15px;
            color: #333;
        }
        
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 10px;
        }
        
        .stat-card {
            background: white;
            padding: 15px 10px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 2px 6px rgba(0,0,0,0.1);
        }
        
        .stat-value {
            font-size: 1.6em;
            font-weight: bold;
            color: #667eea;
            margin-bottom: 4px;
        }
        
        .stat-label {
            color: #666;
            font-size: 0.75em;
            line-height: 1.3;
        }
        
        .stat-card.special {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            grid-column: 1 / -1;
        }
        
        .stat-card.special .stat-value {
            color: white;
            font-size: 2em;
        }
        
        .stat-card.special .stat-label {
            color: rgba(255,255,255,0.95);
            font-size: 0.9em;
        }
        
        .motivation {
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 20px 15px;
            border-radius: 12px;
            text-align: center;
            margin-top: 20px;
            font-size: 1.05em;
            font-style: italic;
            line-height: 1.5;
        }
        
        .chart-container {
            background: white;
            padding: 15px;
            border-radius: 12px;
            margin-top: 15px;
            box-shadow: 0 2px 6px rgba(0,0,0,0.1);
        }
        
        .chart-title {
            font-size: 1em;
            font-weight: bold;
            margin-bottom: 12px;
            color: #333;
        }
        
        .mini-chart {
            display: flex;
            align-items: end;
            height: 80px;
            gap: 4px;
            padding: 8px;
            background: #f8f9fa;
            border-radius: 6px;
        }
        
        .mini-bar {
            flex: 1;
            background: #667eea;
            border-radius: 2px 2px 0 0;
            transition: all 0.3s;
            min-width: 8px;
        }
        
        .mini-bar:hover {
            background: #764ba2;
        }
        
        .sunday-rest {
            grid-column: 1 / -1;
            text-align: center;
            padding: 40px 20px;
            background: linear-gradient(135deg, #f8f9fa, #e9ecef);
            border-radius: 12px;
            border: 2px dashed #dee2e6;
        }
        
        .sunday-rest h2 {
            color: #667eea;
            font-size: 1.5em;
            margin-bottom: 10px;
        }
        
        .sunday-rest p {
            color: #666;
            font-size: 0.95em;
            line-height: 1.5;
        }
        
        @media (min-width: 768px) {
            body {
                padding: 20px;
            }
            
            .header {
                height: 250px;
            }
            
            .header h1 {
                font-size: 2.2em;
            }
            
            .header p {
                font-size: 1.1em;
            }
            
            .content {
                padding: 25px;
            }
            
            .tasks-grid {
                grid-template-columns: repeat(2, 1fr);
                gap: 15px;
            }
            
            .stats-grid {
                grid-template-columns: repeat(3, 1fr);
            }
            
            .stat-card.special {
                grid-column: auto;
            }
        }
        
        @media (min-width: 1024px) {
            .header {
                height: 300px;
            }
            
            .header h1 {
                font-size: 2.5em;
            }
            
            .tasks-grid {
                grid-template-columns: repeat(3, 1fr);
            }
            
            .date-nav button {
                padding: 12px 24px;
                font-size: 14px;
            }
            
            .current-date {
                font-size: 1.2em;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <img id="headerImage" class="header-image" src="" alt="Австрия">
            <div class="header-overlay">
                <h1>🇦🇹 Путь к C1</h1>
                <p>Подготовка к распределительному тесту VWU</p>
                <div class="days-counter">
                    Осталось <span id="daysLeft">0</span> дней
                </div>
            </div>
        </div>
        
        <div class="content">
            <div class="date-nav">
                <button onclick="changeDate(-1)">←</button>
                <div class="current-date" id="currentDate"></div>
                <button onclick="changeDate(1)">→</button>
            </div>
            
            <div class="tasks-grid" id="tasksGrid">
                <!-- Задачи будут здесь -->
            </div>
            
            <div class="stats-section">
                <h2>📊 Общая статистика</h2>
                <div class="stats-grid" id="statsGrid">
                    <!-- Статистика будет здесь -->
                </div>
            </div>
            
            <div class="chart-container">
                <div class="chart-title">Прогресс по месяцам</div>
                <div id="monthlyChart" class="mini-chart"></div>
            </div>
            
            <div class="motivation" id="motivation">
                Начни сегодня — завтра будешь ближе к мечте!
            </div>
        </div>
    </div>

    <script>
        // Данные плана
        const planData = {
            onset: {
                name: 'Onset тесты',
                total: 419,
                daily: 4,
                unit: 'тестов',
                endDate: '2026-06-10',
                type: 'number',
                category: 'test'
            },
            verbs: {
                name: 'Неправильные глаголы',
                total: 200,
                daily: 3,
                unit: 'глаголов',
                endDate: '2026-05-09',
                type: 'number',
                category: 'vocabulary'
            },
            grammarA: {
                name: 'Грамматика A',
                total: 187,
                daily: 6,
                unit: 'стр',
                startDate: '2026-02-09',
                endDate: '2026-03-12',
                type: 'number',
                category: 'grammar',
                order: 1
            },
            grammarB: {
                name: 'Грамматика B',
                total: 268,
                daily: 6,
                unit: 'стр',
                startDate: '2026-03-13',
                endDate: '2026-04-26',
                type: 'number',
                category: 'grammar',
                order: 2
            },
            grammarC: {
                name: 'Грамматика C',
                total: 242,
                daily: 6,
                unit: 'стр',
                startDate: '2026-04-27',
                endDate: '2026-06-07',
                type: 'number',
                category: 'grammar',
                order: 3
            },
            lexiconB1: {
                name: 'Лексика B1',
                total: 300,
                daily: 6,
                unit: 'стр',
                startDate: '2026-02-09',
                endDate: '2026-03-30',
                type: 'number',
                category: 'lexicon',
                order: 1
            },
            lexiconB2: {
                name: 'Лексика B2',
                total: 296,
                daily: 6,
                unit: 'стр',
                startDate: '2026-03-31',
                endDate: '2026-05-19',
                type: 'number',
                category: 'lexicon',
                order: 2
            },
            lexiconC1: {
                name: 'Лексика C1',
                total: 250,
                daily: 6,
                unit: 'стр',
                startDate: '2026-05-20',
                endDate: '2026-07-20',
                type: 'number',
                category: 'lexicon',
                order: 3
            },
            texts: {
                name: 'Тексты',
                total: null,
                daily: 1,
                unit: 'текстов',
                endDate: '2026-07-20',
                type: 'number',
                category: 'practice'
            },
            quizlet: {
                name: 'Quizlet',
                total: null,
                daily: null,
                unit: 'слов',
                endDate: '2026-07-20',
                type: 'number',
                category: 'vocabulary'
            },
            youtube: {
                name: 'YouTube',
                total: null,
                daily: 1,
                unit: 'видео',
                endDate: '2026-07-20',
                type: 'number',
                category: 'practice'
            }
        };
        
        // Мотивирующие фразы
        const motivations = [
            "Отличная работа! Ты на верном пути! 🌟",
            "Каждый день — шаг к мечте! Продолжай! 💪",
            "Ты удивительная! Верь в себя! ✨",
            "Молодец! Немецкий язык тебе покорится! 🇩🇪",
            "Сегодняшние усилия — завтрашний успех! 🎯",
            "Ты сильнее, чем думаешь! Вперёд! 🚀",
            "Отличный прогресс! Так держать! 👏",
            "Ты создаёшь своё будущее прямо сейчас! 🌈",
            "Великолепно! Австрия ждёт тебя! 🏔️",
            "Ты справишься! Я в тебя верю! 💫"
        ];
        
        // Фото Австрии
        const austriaImages = [
            'https://images.unsplash.com/photo-1516550893923-42d28e5677af?w=800',
            'https://images.unsplash.com/photo-1596484552834-6a58f850e0a1?w=800',
            'https://images.unsplash.com/photo-1531366936337-7c912a4589a7?w=800',
            'https://images.unsplash.com/photo-1506905925346-21bda4d32df4?w=800',
            'https://images.unsplash.com/photo-1491553895911-0055uj3a34?w=800',
            'https://images.unsplash.com/photo-1476514525535-07fb3b4ae5f1?w=800',
            'https://images.unsplash.com/photo-1501785888041-af3ef285b470?w=800',
            'https://images.unsplash.com/photo-1464822759023-fed622ff2c3b?w=800'
        ];
        
        let currentDate = new Date('2026-02-09');
        const endDate = new Date('2026-07-20');
        const startDate = new Date('2026-02-09');
        
        function loadData() {
            const saved = localStorage.getItem('germanStudyPlan');
            return saved ? JSON.parse(saved) : {};
        }
        
        function saveData(data) {
            localStorage.setItem('germanStudyPlan', JSON.stringify(data));
        }
        
        let studyData = loadData();
        
        function getDateKey(date) {
            return date.toISOString().split('T')[0];
        }
        
        function isSunday(date) {
            return date.getDay() === 0;
        }
        
        function getActiveBook(category, date) {
            const books = Object.entries(planData)
                .filter(([k, p]) => p.category === category && p.order)
                .sort((a, b) => a[1].order - b[1].order);
            
            for (const [key, plan] of books) {
                const bookStart = new Date(plan.startDate);
                const bookEnd = new Date(plan.endDate);
                if (date >= bookStart && date <= bookEnd) {
                    return key;
                }
            }
            return null;
        }
        
        function getDailyPlan(date, key) {
            const plan = planData[key];
            
            if (plan.category === 'grammar' || plan.category === 'lexicon') {
                const activeBook = getActiveBook(plan.category, date);
                if (activeBook !== key) return null;
            }
            
            const blockStart = plan.startDate ? new Date(plan.startDate) : startDate;
            const blockEnd = new Date(plan.endDate);
            
            if (date < blockStart || date > blockEnd) {
                return null;
            }
            
            const done = getTotalDone(key, date);
            if (plan.total && done >= plan.total) {
                return null;
            }
            
            return plan.daily || 0;
        }
        
        function getTotalDone(key, untilDate) {
            let total = 0;
            
            for (let d = new Date(startDate); d <= untilDate; d.setDate(d.getDate() + 1)) {
                const dk = getDateKey(d);
                if (studyData[dk] && studyData[dk][key]) {
                    total += parseInt(studyData[dk][key]) || 0;
                }
            }
            return total;
        }
        
        function getRemaining(key, date) {
            const plan = planData[key];
            if (!plan.total) return null;
            const done = getTotalDone(key, date);
            return Math.max(0, plan.total - done);
        }
        
        function changeDate(days) {
            currentDate.setDate(currentDate.getDate() + days);
            
            while (isSunday(currentDate)) {
                currentDate.setDate(currentDate.getDate() + (days > 0 ? 1 : -1));
            }
            
            render();
        }
        
        function saveInput(key, value) {
            const dateKey = getDateKey(currentDate);
            if (!studyData[dateKey]) {
                studyData[dateKey] = {};
            }
            studyData[dateKey][key] = value;
            saveData(studyData);
            render();
        }
        
        function getStatus(key, plan, done) {
            if (!plan) return 'not-started';
            if (done >= plan) return 'completed';
            if (done > 0) return 'partial';
            return 'not-started';
        }
        
        function renderTasks() {
            const grid = document.getElementById('tasksGrid');
            const dateKey = getDateKey(currentDate);
            const todayData = studyData[dateKey] || {};
            
            if (isSunday(currentDate)) {
                grid.innerHTML = `
                    <div class="sunday-rest">
                        <h2>🌴 Воскресенье</h2>
                        <p>День отдыха! Восстанавливай силы.<br>Завтра продолжим с новой энергией!</p>
                    </div>
                `;
                return;
            }
            
            let html = '';
            
            for (const [key, plan] of Object.entries(planData)) {
                const dailyPlan = getDailyPlan(currentDate, key);
                if (dailyPlan === null && plan.category !== 'practice' && plan.category !== 'vocabulary') continue;
                
                const done = todayData[key] || 0;
                const totalDone = getTotalDone(key, currentDate);
                const remaining = getRemaining(key, currentDate);
                const status = getStatus(key, dailyPlan, parseInt(done));
                const percent = plan.total ? Math.min(100, (totalDone / plan.total) * 100) : 0;
                
                html += `
                    <div class="task-card ${status}">
                        <div class="task-header">
                            <div class="task-title">${plan.name}</div>
                            <div class="task-status status-${status}">
                                ${status === 'completed' ? '✓' : status === 'partial' ? '◐' : '○'}
                            </div>
                        </div>
                        
                        ${dailyPlan ? `
                            <div class="task-plan">
                                📋 План: <strong>${dailyPlan} ${plan.unit}</strong>
                            </div>
                        ` : ''}
                        
                        <div class="task-input">
                            <input type="number" min="0" placeholder="Сколько сделала" value="${done || ''}" 
                                   onchange="saveInput('${key}', this.value)">
                            <button onclick="saveInput('${key}', this.previousElementSibling.value)">✓</button>
                        </div>
                        
                        <div class="task-progress">
                            <div class="progress-bar">
                                <div class="progress-fill" style="width: ${percent}%"></div>
                            </div>
                            <div class="progress-text">
                                ${totalDone}${plan.total ? '/' + plan.total : ''} ${plan.unit}${remaining !== null ? ' · ост. ' + remaining : ''}
                            </div>
                        </div>
                    </div>
                `;
            }
            
            grid.innerHTML = html;
        }
        
        function renderStats() {
            const grid = document.getElementById('statsGrid');
            let html = '';
            
            for (const [key, plan] of Object.entries(planData)) {
                if (!plan.total) continue;
                const done = getTotalDone(key, currentDate);
                const percent = Math.round((done / plan.total) * 100);
                
                html += `
                    <div class="stat-card">
                        <div class="stat-value">${percent}%</div>
                        <div class="stat-label">${plan.name}</div>
                    </div>
                `;
            }
            
            const grammarBooks = ['grammarA', 'grammarB', 'grammarC'];
            const lexiconBooks = ['lexiconB1', 'lexiconB2', 'lexiconC1'];
            const allBooks = [...grammarBooks, ...lexiconBooks];
            
            let completedBooks = 0;
            allBooks.forEach(key => {
                if (getTotalDone(key, currentDate) >= planData[key].total) {
                    completedBooks++;
                }
            });
            
            html += `
                <div class="stat-card special">
                    <div class="stat-value">${completedBooks}/${allBooks.length}</div>
                    <div class="stat-label">Учебников завершено</div>
                </div>
            `;
            
            grid.innerHTML = html;
        }
        
        function renderChart() {
            const chart = document.getElementById('monthlyChart');
            const months = ['Фев', 'Мар', 'Апр', 'Май', 'Июн', 'Июл'];
            let html = '';
            
            months.forEach((month, idx) => {
                const monthEnd = new Date(2026, 2 + idx, 9);
                
                let monthProgress = 0;
                let count = 0;
                
                for (const [key, plan] of Object.entries(planData)) {
                    if (!plan.total) continue;
                    const done = getTotalDone(key, monthEnd);
                    const percent = Math.min(100, (done / plan.total) * 100);
                    monthProgress += percent;
                    count++;
                }
                
                const avgProgress = count > 0 ? monthProgress / count : 0;
                const height = Math.max(10, avgProgress);
                
                html += `<div class="mini-bar" style="height: ${height}%;" title="${month}: ${Math.round(avgProgress)}%"></div>`;
            });
            
            chart.innerHTML = html;
        }
        
        function updateImage() {
            const img = document.getElementById('headerImage');
            const dayOfYear = Math.floor((currentDate - startDate) / (1000 * 60 * 60 * 24));
            const imageIndex = dayOfYear % austriaImages.length;
            img.src = austriaImages[imageIndex];
        }
        
        function updateDaysCounter() {
            const daysLeft = Math.ceil((endDate - currentDate) / (1000 * 60 * 60 * 24));
            document.getElementById('daysLeft').textContent = Math.max(0, daysLeft);
        }
        
        function updateMotivation() {
            const dateKey = getDateKey(currentDate);
            const todayData = studyData[dateKey] || {};
            const hasProgress = Object.values(todayData).some(v => v && v !== '0');
            
            if (hasProgress) {
                const dayOfYear = Math.floor((currentDate - startDate) / (1000 * 60 * 60 * 24));
                const motivationIndex = dayOfYear % motivations.length;
                document.getElementById('motivation').textContent = motivations[motivationIndex];
            }
        }
        
        function updateDate() {
            const options = { weekday: 'short', day: 'numeric', month: 'short' };
            document.getElementById('currentDate').textContent = currentDate.toLocaleDateString('ru-RU', options);
        }
        
        function render() {
            updateDate();
            updateImage();
            updateDaysCounter();
            renderTasks();
            renderStats();
            renderChart();
            updateMotivation();
        }
        
        render();
    </script>
</body>
</html>
