<!DOCTYPE html>
<html lang="zh-TW">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MOI 2025 - 澳門奧林匹克資訊競賽</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', 'Microsoft JhengHei', sans-serif;
        }
        
        body {
            background-color: #f5f7fa;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            background: linear-gradient(135deg, #1a3a8f 0%, #2a5caa 100%);
            color: white;
            padding: 30px 0;
            text-align: center;
            border-radius: 0 0 10px 10px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            margin-bottom: 30px;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            font-weight: 700;
        }
        
        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
        }
        
        .tabs {
            display: flex;
            justify-content: center;
            margin-bottom: 30px;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .tab {
            padding: 12px 24px;
            background-color: white;
            border-radius: 30px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            border: 2px solid transparent;
        }
        
        .tab:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .tab.active {
            background-color: #1a3a8f;
            color: white;
            border-color: #0d2568;
        }
        
        .table-container {
            background-color: white;
            border-radius: 10px;
            overflow: hidden;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            margin-bottom: 30px;
        }
        
        table {
            width: 100%;
            border-collapse: collapse;
        }
        
        thead {
            background-color: #1a3a8f;
            color: white;
        }
        
        th {
            padding: 16px 12px;
            text-align: left;
            font-weight: 600;
        }
        
        tbody tr {
            border-bottom: 1px solid #eaeaea;
            transition: background-color 0.2s;
        }
        
        tbody tr:hover {
            background-color: #f8f9ff;
        }
        
        td {
            padding: 14px 12px;
        }
        
        .rank-1 {
            background-color: #fff9e6;
            font-weight: bold;
        }
        
        .gold {
            color: #d4af37;
            font-weight: bold;
        }
        
        .silver {
            color: #c0c0c0;
            font-weight: bold;
        }
        
        .bronze {
            color: #cd7f32;
            font-weight: bold;
        }
        
        .score {
            font-weight: 600;
            text-align: center;
        }
        
        .perfect-score {
            background-color: #e8f5e9;
            color: #2e7d32;
        }
        
        .medal-count {
            display: flex;
            justify-content: center;
            gap: 30px;
            margin-bottom: 30px;
            flex-wrap: wrap;
        }
        
        .medal-card {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 3px 10px rgba(0, 0, 0, 0.08);
            text-align: center;
            min-width: 150px;
        }
        
        .medal-card.gold {
            border-top: 4px solid #d4af37;
        }
        
        .medal-card.silver {
            border-top: 4px solid #c0c0c0;
        }
        
        .medal-card.bronze {
            border-top: 4px solid #cd7f32;
        }
        
        .medal-count-number {
            font-size: 2.5rem;
            font-weight: bold;
            margin: 10px 0;
        }
        
        footer {
            text-align: center;
            padding: 20px;
            margin-top: 40px;
            color: #666;
            font-size: 0.9rem;
            border-top: 1px solid #eaeaea;
        }
        
        @media (max-width: 768px) {
            .table-container {
                overflow-x: auto;
            }
            
            table {
                min-width: 700px;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            .tab {
                padding: 10px 16px;
                font-size: 0.9rem;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>MOI 2025</h1>
            <p class="subtitle">澳門奧林匹克資訊競賽</p>
        </div>
    </header>
    
    <div class="container">
        <div class="tabs">
            <div class="tab active">比賽概況</div>
            <div class="tab">比賽章程</div>
            <div class="tab">MOIP</div>
            <div class="tab">MOIJ</div>
            <div class="tab">MOIS</div>
            <div class="tab">MOIC</div>
        </div>
        
        <div class="medal-count">
            <div class="medal-card gold">
                <h3>金獎</h3>
                <div class="medal-count-number">5</div>
                <p>獲獎者</p>
            </div>
            <div class="medal-card silver">
                <h3>銀獎</h3>
                <div class="medal-count-number">2</div>
                <p>獲獎者</p>
            </div>
            <div class="medal-card bronze">
                <h3>銅獎</h3>
                <div class="medal-count-number">0</div>
                <p>獲獎者</p>
            </div>
        </div>
        
        <div class="table-container">
            <table>
                <thead>
                    <tr>
                        <th>排名</th>
                        <th>姓名</th>
                        <th>學校</th>
                        <th>multiples</th>
                        <th>rock</th>
                        <th>simclock</th>
                        <th>總分</th>
                        <th>獎項</th>
                    </tr>
                </thead>
                <tbody>
                    <tr class="rank-1">
                        <td>1</td>
                        <td>吳卓恆</td>
                        <td>勞校中學附屬小學</td>
                        <td class="score perfect-score">100</td>
                        <td class="score perfect-score">100</td>
                        <td class="score perfect-score">100</td>
                        <td class="score">300</td>
                        <td class="gold">金獎</td>
                    </tr>
                    <tr class="rank-1">
                        <td>1</td>
                        <td>曾子睿</td>
                        <td>勞校中學附屬小學</td>
                        <td class="score perfect-score">100</td>
                        <td class="score perfect-score">100</td>
                        <td class="score perfect-score">100</td>
                        <td class="score">300</td>
                        <td class="gold">金獎</td>
                    </tr>
                    <tr class="rank-1">
                        <td>1</td>
                        <td>溫庭昊</td>
                        <td>培正中學</td>
                        <td class="score perfect-score">100</td>
                        <td class="score perfect-score">100</td>
                        <td class="score perfect-score">100</td>
                        <td class="score">300</td>
                        <td class="gold">金獎</td>
                    </tr>
                    <tr class="rank-1">
                        <td>1</td>
                        <td>曾繁宇</td>
                        <td>培正中學</td>
                        <td class="score perfect-score">100</td>
                        <td class="score perfect-score">100</td>
                        <td class="score perfect-score">100</td>
                        <td class="score">300</td>
                        <td class="gold">金獎</td>
                    </tr>
                    <tr class="rank-1">
                        <td>1</td>
                        <td>沈以恆</td>
                        <td>培正中學</td>
                        <td class="score perfect-score">100</td>
                        <td class="score perfect-score">100</td>
                        <td class="score perfect-score">100</td>
                        <td class="score">300</td>
                        <td class="gold">金獎</td>
                    </tr>
                    <tr>
                        <td>6</td>
                        <td>謝皓匡</td>
                        <td>培正中學</td>
                        <td class="score perfect-score">100</td>
                        <td class="score perfect-score">100</td>
                        <td class="score">90</td>
                        <td class="score">290</td>
                        <td class="silver">銀獎</td>
                    </tr>
                    <tr>
                        <td>6</td>
                        <td>李沛穎</td>
                        <td>培正中學</td>
                        <td class="score perfect-score">100</td>
                        <td class="score perfect-score">100</td>
                        <td class="score">90</td>
                        <td class="score">290</td>
                        <td class="silver">銀獎</td>
                    </tr>
                </tbody>
            </table>
        </div>
    </div>
    
    <footer>
        <div class="container">
            <p>MOI 2025 - 澳門奧林匹克資訊競賽 &copy; 2025 版權所有</p>
        </div>
    </footer>

    <script>
        // 标签切换功能
        document.querySelectorAll('.tab').forEach(tab => {
            tab.addEventListener('click', function() {
                document.querySelectorAll('.tab').forEach(t => t.classList.remove('active'));
                this.classList.add('active');
            });
        });
        
        // 添加表格行悬停效果
        document.querySelectorAll('tbody tr').forEach(row => {
            row.addEventListener('mouseenter', function() {
                this.style.transform = 'scale(1.01)';
                this.style.boxShadow = '0 5px 15px rgba(0, 0, 0, 0.1)';
            });
            
            row.addEventListener('mouseleave', function() {
                this.style.transform = 'scale(1)';
                this.style.boxShadow = 'none';
            });
        });
    </script>
</body>
</html>
