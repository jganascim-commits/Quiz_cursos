<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Descubra DS - Desenvolvimento de Sistemas</title>
    <style>
        :root {
            --primary: #6366f1;
            --primary-dark: #4f46e5;
            --accent: #ec4899;
            --bg-color: #0f172a;
            --card-bg: #1e293b;
            --text-color: #f8fafc;
            --text-muted: #94a3b8;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            line-height: 1.6;
            padding: 20px;
        }

        .container {
            max-width: 800px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            text-align: center;
            margin-bottom: 40px;
        }

        header h1 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 10px;
        }

        header p {
            color: var(--text-muted);
            font-size: 1.1rem;
        }

        /* Seção de História / Mulheres na Tech */
        .history-section {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 30px;
            margin-bottom: 40px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.3);
            border-left: 5px solid var(--accent);
        }

        .history-section h2 {
            color: var(--accent);
            margin-bottom: 15px;
            font-size: 1.8rem;
        }

        .history-section p {
            margin-bottom: 15px;
            color: #cbd5e1;
        }

        .pioneer-card {
            background: rgba(255, 255, 255, 0.05);
            padding: 15px;
            border-radius: 8px;
            margin-top: 15px;
        }

        .pioneer-card h3 {
            color: #f43f5e;
            font-size: 1.2rem;
            margin-bottom: 5px;
        }

        /* Quiz Container */
        .quiz-container {
            background: var(--card-bg);
            border-radius: 12px;
            padding: 30px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.3);
        }

        .question-box {
            margin-bottom: 25px;
        }

        .question-box h3 {
            font-size: 1.2rem;
            margin-bottom: 15px;
            color: #e2e8f0;
        }

        .options {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }

        .option-label {
            background: rgba(255, 255, 255, 0.05);
            padding: 12px 15px;
            border-radius: 8px;
            cursor: pointer;
            transition: all 0.3s ease;
            border: 1px solid transparent;
        }

        .option-label:hover {
            background: rgba(99, 102, 241, 0.1);
            border-color: var(--primary);
        }

        .option-label input {
            margin-right: 10px;
        }

        button.submit-btn {
            background-color: var(--primary);
            color: white;
            border: none;
            padding: 12px 25px;
            font-size: 1rem;
            font-weight: bold;
            border-radius: 8px;
            cursor: pointer;
            width: 100%;
            transition: background 0.3s;
        }

        button.submit-btn:hover {
            background-color: var(--primary-dark);
        }

        /* Resultado */
        .result-box {
            display: none;
            text-align: center;
            padding: 20px;
        }

        .result-box h2 {
            color: #34d399;
            font-size: 2rem;
            margin-bottom: 15px;
        }

        .result-box p {
            font-size: 1.1rem;
            color: #cbd5e1;
            margin-bottom: 20px;
        }
    </style>
</head>
<body>

    <div class="container">
        <header>
            <h1>Desenvolvimento de Sistemas (DS)</h1>
            <p>Conheça a história, quebre barreiras e descubra se a programação é para você!</p>
        </header>

        <!-- Seção: Mulheres que Revolucionaram a Programação -->
        <section class="history-section">
            <h2>💻 A História e o Protótipo Feminino em DS</h2>
            <p>Você sabia que a programação nasceu pelas mãos de uma mulher? Em 1840, <strong>Ada Lovelace</strong> escreveu o primeiro algoritmo da história. Desde então, as mulheres sempre estiveram na vanguarda da tecnologia.</p>
            
            <div class="pioneer-card">
                <h3>🚀 Margaret Hamilton e a Missão Apollo 11</h3>
                <p>Quando o homem pisou na Lua em 1969, o computador de bordo da nave quase falhou por sobrecarga. A única coisa que salvou a missão foi o sistema de software infalível desenvolvido por uma equipe liderada por <strong>Margaret Hamilton</strong> (diretora de engenharia de software do projeto). Ela é literalmente a criadora da engenharia de software moderna!</p>
            </div>
            <p style="margin-top: 15px;">Portanto, tecnologia é lugar de <strong>qualquer pessoa</strong> que tenha paixão por criar, inovar e resolver problemas. O código não vê gênero, vê talento!</p>
        </section>

        <!-- Seção: Quiz Interativo -->
        <div class="quiz-container" id="quiz-card">
            <form id="dsQuiz">
                
                <!-- Pergunta 1 -->
                <div class="question-box">
                    <h3>1. Você está jogando um game ou usando um app e do nada ele trava com um bug bizarro. Qual é a sua reação?</h3>
                    <div class="options">
                        <label class="option-label"><input type="radio" name="q1" value="1"> Passar raiva, fecho o app e vou fazer outra coisa.</label>
                        <label class="option-label"><input type="radio" name="q1" value="2"> Acho chato, mas espero voltar a funcionar.</label>
                        <label class="option-label"><input type="radio" name="q1" value="3" required> Fico curioso tentando entender *por que* deu ruim e testar de novo!</label>
                    </div>
                </div>

                <!-- Pergunta 2 -->
                <div class="question-box">
                    <h3>2. Se você pudesse ter um superpoder digital hoje, qual escolheria?</h3>
                    <div class="options">
                        <label class="option-label"><input type="radio" name="q2" value="1"> Ter acesso a todos os apps do mundo de graça.</label>
                        <label class="option-label"><input type="radio" name="q2" value="2"> Personalizar e configurar meu celular/computador ao máximo.</label>
                        <label class="option-label"><input type="radio" name="q2" value="3" required> Criar o meu próprio jogo, site ou aplicativo do zero.</label>
                    </div>
                </div>

                <!-- Pergunta 3 -->
                <div class="question-box">
                    <h3>3. Sabe aquela tarefa chata e repetitiva? Como sua mente funciona?</h3>
                    <div class="options">
                        <label class="option-label"><input type="radio" name="q3" value="1"> Faço logo rezando para acabar.</label>
                        <label class="option-label"><input type="radio" name="q3" value="2"> Deixo para o último minuto.</label>
                        <label class="option-label"><input type="radio" name="q3" value="3" required> Penso: "Deve existir um jeito ou um código para automatizar isso e fazer em segundos."</label>
                    </div>
                </div>

                <!-- Pergunta 4 -->
                <div class="question-box">
                    <h3>4. Quando você descobre que redes sociais usam algoritmos complexos para recomendar conteúdos, você:</h3>
                    <div class="options">
                        <label class="option-label"><input type="radio" name="q4" value="1"> Nem ligo, só quero ver o feed.</label>
                        <label class="option-label"><input type="radio" name="q4" value="2"> Acho meio estranho, mas continuo usando.</label>
                        <label class="option-label"><input type="radio" name="q4" value="3" required> Acho fascinante! Queria ver a lógica e as linhas de código por trás disso.</label>
                    </div>
                </div>

                <!-- Pergunta 5 -->
                <div class="question-box">
                    <h3>5. Se falta só UMA peça ou detalhe para um projeto dar certo, mas não encaixa, você:</h3>
                    <div class="options">
                        <label class="option-label"><input type="radio" name="q5" value="1"> Largo mão, já deu o meu tempo.</label>
                        <label class="option-label"><input type="radio" name="q5" value="2"> Peço para outra pessoa resolver.</label>
                        <label class="option-label"><input type="radio" name="q5" value="3" required> Fico obstinado! Não sossego enquanto não achar o erro e fizer funcionar.</label>
                    </div>
                </div>

                <button type="button" class="submit-btn" onclick="calcularResultado()">Ver Meu Resultado</button>
            </form>
        </div>

        <!-- Caixa de Resultado -->
        <div class="quiz-container result-box" id="result-card">
            <h2 id="result-title"></h2>
            <p id="result-text"></p>
            <button class="submit-btn" onclick="reiniciarQuiz()">Refazer Quiz</button>
        </div>
    </div>

    <script>
        function calcularResultado() {
            const q1 = document.querySelector('input[name="q1"]:checked');
            const q2 = document.querySelector('input[name="q2"]:checked');
            const q3 = document.querySelector('input[name="q3"]:checked');
            const q4 = document.querySelector('input[name="q4"]:checked');
            const q5 = document.querySelector('input[name="q5"]:checked');

            if (!q1 || !q2 || !q3 || !q4 || !q5) {
                alert("Por favor, responda todas as perguntas antes de ver o resultado!");
                return;
            }

            let soma = parseInt(q1.value) + parseInt(q2.value) + parseInt(q3.value) + parseInt(q4.value) + parseInt(q5.value);

            let titulo = "";
            let mensagem = "";

            if (soma >= 12) {
                titulo = "🚀 Dev Nato(a)!";
                mensagem = "Você tem a mente analítica, curiosa e focada em solução de problemas que o mercado de tecnologia procura. O curso de Desenvolvimento de Sistemas tem tudo a ver com o seu perfil!";
            } else if (soma >= 8) {
                titulo = "💡 Perfil Explorador(a)!";
                mensagem = "Você tem bastante potencial e curiosidade tecnológica. O curso de DS vai te dar as ferramentas perfeitas para transformar essa curiosidade em projetos reais!";
            } else {
                titulo = "🎨 Perfil Criativo / Outras Áreas!";
                mensagem = "Talvez código puro não seja sua primeira escolha, mas lembre-se: a tecnologia apoia todas as profissões. Vale a pena conhecer o curso para entender como a inovação funciona!";
            }

            document.getElementById("quiz-card").style.display = "none";
            document.getElementById("result-card").style.display = "block";
            document.getElementById("result-title").innerText = titulo;
            document.getElementById("result-text").innerText = mensagem;
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        function reiniciarQuiz() {
            document.getElementById("dsQuiz").reset();
            document.getElementById("result-card").style.display = "none";
            document.getElementById("quiz-card").style.display = "block";
        }
    </script>
</body>
</html>
