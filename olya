<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">
    <title>Interactive Vocabulary Exercise | Film & Performance Terms</title>
    <style>
        * {
            box-sizing: border-box;
        }

        body {
            background: linear-gradient(135deg, #1a1e2b 0%, #2a2f3f 100%);
            font-family: 'Segoe UI', 'Poppins', 'Roboto', sans-serif;
            margin: 0;
            padding: 30px 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
        }

        .exercise-card {
            max-width: 950px;
            width: 100%;
            background: #fefcf0;
            background-image: radial-gradient(circle at 10% 20%, rgba(255,245,215,0.4) 2%, transparent 2.5%);
            background-size: 28px 28px;
            border-radius: 56px;
            box-shadow: 0 30px 50px rgba(0, 0, 0, 0.4), 0 0 0 1px rgba(255, 215, 150, 0.3);
            overflow: hidden;
            transition: all 0.2s;
        }

        /* header with cinematic style */
        .exercise-header {
            background: #0f0e17;
            padding: 28px 36px;
            text-align: center;
            border-bottom: 4px solid #ffc857;
        }

        .exercise-header h1 {
            margin: 0;
            font-size: 2.1rem;
            letter-spacing: -0.5px;
            background: linear-gradient(135deg, #FFE6B0, #FFB347);
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
            font-weight: 700;
        }

        .exercise-header p {
            margin: 8px 0 0;
            color: #b9c8ff;
            font-weight: 500;
            font-size: 0.95rem;
        }

        .instruction {
            background: #2e2a3e;
            color: #f5e7c8;
            padding: 12px 28px;
            font-size: 0.95rem;
            display: flex;
            align-items: center;
            gap: 12px;
            flex-wrap: wrap;
            border-bottom: 1px solid #4a3f5e;
        }

        .instruction-icon {
            font-size: 1.4rem;
        }

        /* content */
        .content-pane {
            padding: 30px 36px 36px;
        }

        /* word bank */
        .word-bank {
            background: #1e293b;
            border-radius: 48px;
            padding: 16px 24px;
            margin-bottom: 32px;
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 14px;
            box-shadow: inset 0 1px 3px rgba(0,0,0,0.2), 0 8px 12px -6px rgba(0,0,0,0.2);
        }

        .word-chip {
            background: #ffedd5;
            color: #7c2d12;
            font-weight: 700;
            font-size: 1.1rem;
            padding: 8px 22px;
            border-radius: 60px;
            letter-spacing: 0.3px;
            box-shadow: 0 2px 6px rgba(0,0,0,0.2);
            font-family: monospace;
            transition: 0.1s;
            border: 1px solid #ffcd94;
        }

        .word-chip span {
            font-weight: 600;
        }

        /* sentences list */
        .sentences-list {
            display: flex;
            flex-direction: column;
            gap: 20px;
            margin-bottom: 32px;
        }

        .sentence-card {
            background: white;
            border-radius: 32px;
            padding: 16px 22px;
            box-shadow: 0 5px 12px rgba(0, 0, 0, 0.05);
            transition: all 0.2s;
            border: 1px solid #f0e2c0;
        }

        .sentence-text {
            font-size: 1.06rem;
            line-height: 1.45;
            color: #1e1b2c;
            font-weight: 500;
            margin-bottom: 14px;
            display: flex;
            flex-wrap: wrap;
            align-items: baseline;
            gap: 8px;
        }

        .blank-highlight {
            display: inline-block;
            min-width: 160px;
        }

        .blank-highlight input {
            padding: 10px 16px;
            font-size: 0.95rem;
            border: 2px solid #d6c6a0;
            border-radius: 60px;
            width: 180px;
            text-align: center;
            font-family: 'Segoe UI', monospace;
            font-weight: 500;
            background: #fffef7;
            transition: 0.15s;
        }

        .blank-highlight input:focus {
            border-color: #ffb347;
            outline: none;
            box-shadow: 0 0 0 3px rgba(255, 180, 71, 0.2);
            background: white;
        }

        .feedback-area {
            margin-top: 10px;
            font-size: 0.85rem;
            padding-left: 8px;
            color: #4b5563;
            font-weight: 500;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .status-icon {
            font-size: 1.1rem;
        }

        /* buttons */
        .action-buttons {
            display: flex;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 15px;
            margin-top: 8px;
        }

        .btn {
            border: none;
            padding: 12px 26px;
            border-radius: 44px;
            font-weight: 700;
            font-size: 0.9rem;
            cursor: pointer;
            transition: all 0.2s ease;
            font-family: inherit;
            background: #eef2ff;
            color: #1f2a44;
        }

        .btn-primary {
            background: #f08c2e;
            color: white;
            box-shadow: 0 3px 6px rgba(0,0,0,0.15);
        }

        .btn-primary:hover {
            background: #d9771e;
            transform: translateY(-2px);
        }

        .btn-secondary {
            background: #cbd5e6;
            color: #1f2937;
        }

        .btn-secondary:hover {
            background: #b9c4da;
        }

        .score-panel {
            background: #f8f2e3;
            border-radius: 40px;
            padding: 14px 20px;
            text-align: center;
            margin-top: 28px;
            font-weight: bold;
            font-size: 1.1rem;
            color: #3b2c1e;
            border: 1px solid #eeddbb;
        }

        .perfect-badge {
            background: #d1fae5;
            color: #065f46;
        }

        footer {
            background: #181d2b;
            text-align: center;
            font-size: 0.7rem;
            padding: 14px;
            color: #7e8aa2;
            border-top: 1px solid #2b3348;
        }

        @media (max-width: 650px) {
            .content-pane {
                padding: 20px;
            }
            .blank-highlight input {
                width: 140px;
                padding: 8px 10px;
            }
            .word-chip {
                font-size: 0.9rem;
                padding: 5px 16px;
            }
        }
    </style>
</head>
<body>
<div class="exercise-card">
    <div class="exercise-header">
        <h1>🎬 Cinema & Performance Vocabulary</h1>
        <p>Fill in each blank with the correct term from the word bank</p>
    </div>
    <div class="instruction">
        <div class="instruction-icon">🎭</div>
        <div><strong>📖 Word Bank:</strong> Choose from the five terms below. Each word is used exactly once.</div>
    </div>
    <div class="content-pane">
        <!-- Word Bank display -->
        <div class="word-bank">
            <div class="word-chip"><span>🎭 mise‑en‑scène</span></div>
            <div class="word-chip"><span>🌀 illusion</span></div>
            <div class="word-chip"><span>⚖️ ethics</span></div>
            <div class="word-chip"><span>✂️ editing</span></div>
            <div class="word-chip"><span>🎩 misdirection</span></div>
        </div>

        <!-- Sentences container (will be generated by JS) -->
        <div class="sentences-list" id="sentencesContainer"></div>

        <div class="action-buttons">
            <button class="btn btn-primary" id="checkBtn">✨ Check Answers</button>
            <button class="btn btn-secondary" id="resetBtn">⟳ Clear All</button>
        </div>
        <div id="scorePanel" class="score-panel">
            ⚡ Ready — fill in the blanks and press 'Check Answers'
        </div>
    </div>
    <footer>
        🎬 The Four Horsemen · Film Terminology Exercise | Interactive worksheet
    </footer>
</div>

<script>
    // ----- Vocabulary data definition -----
    // correct answers: each sentence has an id and the correct term
    const sentencesData = [
        {
            id: 0,
            text: "The Four Horsemen use _____________ during performances to distract the audience.",
            correctAnswer: "misdirection"
        },
        {
            id: 1,
            text: "Rapid changes from the stage show to the police investigation are examples of _____________ choices.",
            correctAnswer: "editing"
        },
        {
            id: 2,
            text: "When a film makes viewers feel unsure about what actually happened, it creates _____________.",
            correctAnswer: "illusion"
        },
        {
            id: 3,
            text: "Redistributing stolen money to audience members raises questions about _____________.",
            correctAnswer: "ethics"
        },
        {
            id: 4,
            text: "The combination of set design, costume, and props is part of the film's _____________.",
            correctAnswer: "mise-en-scène"
        }
    ];

    // normalization: we will accept minor variations but strict matches the exact term (lowercase compare)
    // but also handle possible accents? We'll map correct answer with lowercase trimmed.
    // Also allow "mise-en-scène" with or without accent? user might type "mise en scene"? But to keep clean: 
    // we provide word bank and we match based on exact term (case insensitive). 
    // We will accept common variations for mise‑en‑scène: "mise-en-scène", "mise en scene", but better to match word bank representation.
    // however the strict correct answer stored is "mise-en-scène". We'll also accept 'mise en scene' for better UX.
    // but to be fair: we tell students use words from bank -> we check normalized.
    function normalizeAnswer(input) {
        let cleaned = input.trim().toLowerCase();
        // special handling for mise‑en‑scène different dashes and spaces
        if (cleaned === "mise-en-scène" || cleaned === "mise en scene" || cleaned === "miseenscène" || cleaned === "mise-en-scene" || cleaned === "mise en scène") {
            return "mise-en-scène";
        }
        // for others: just return cleaned version of the term
        if (cleaned === "misdirection") return "misdirection";
        if (cleaned === "editing") return "editing";
        if (cleaned === "illusion") return "illusion";
        if (cleaned === "ethics") return "ethics";
        return cleaned;
    }

    // store references to all input elements
    let sentenceInputs = [];

    // Render questions dynamically
    function renderSentences() {
        const container = document.getElementById("sentencesContainer");
        container.innerHTML = "";
        sentenceInputs = [];

        sentencesData.forEach((sentence, idx) => {
            const sentenceCard = document.createElement("div");
            sentenceCard.className = "sentence-card";
            sentenceCard.dataset.idx = idx;

            const sentenceDiv = document.createElement("div");
            sentenceDiv.className = "sentence-text";

            // split text around the placeholder "_____________"
            const placeholder = "_____________";
            const parts = sentence.text.split(placeholder);
            
            // left part
            if (parts[0]) {
                const leftSpan = document.createElement("span");
                leftSpan.textContent = parts[0];
                sentenceDiv.appendChild(leftSpan);
            }
            
            // input field for blank
            const inputWrapper = document.createElement("div");
            inputWrapper.className = "blank-highlight";
            const inputField = document.createElement("input");
            inputField.type = "text";
            inputField.placeholder = "type term...";
            inputField.id = `input_${idx}`;
            inputField.autocomplete = "off";
            inputWrapper.appendChild(inputField);
            sentenceDiv.appendChild(inputWrapper);
            
            // right part after placeholder
            if (parts[1]) {
                const rightSpan = document.createElement("span");
                rightSpan.textContent = parts[1];
                sentenceDiv.appendChild(rightSpan);
            }
            
            // feedback area
            const feedbackDiv = document.createElement("div");
            feedbackDiv.className = "feedback-area";
            feedbackDiv.id = `feedback_${idx}`;
            feedbackDiv.innerHTML = `<span class="status-icon">⏳</span> <span>Not answered yet</span>`;
            
            sentenceCard.appendChild(sentenceDiv);
            sentenceCard.appendChild(feedbackDiv);
            container.appendChild(sentenceCard);
            
            sentenceInputs.push(inputField);
        });
    }

    // function to check all answers
    function checkAllAnswers() {
        let correctCount = 0;
        const total = sentencesData.length;
        
        for (let i = 0; i < sentencesData.length; i++) {
            const userRaw = sentenceInputs[i].value.trim();
            const normalizedUser = normalizeAnswer(userRaw);
            const correctRaw = sentencesData[i].correctAnswer;
            // for misc correctAnswer we also normalize to lower but correctAnswer stored as expected string.
            let isCorrect = false;
            if (correctRaw === "mise-en-scène") {
                // if normalized matches the canonical form
                if (normalizedUser === "mise-en-scène") isCorrect = true;
            } else {
                if (normalizedUser === correctRaw.toLowerCase()) isCorrect = true;
            }
            
            const feedbackDiv = document.getElementById(`feedback_${i}`);
            const inputElement = sentenceInputs[i];
            
            if (isCorrect) {
                correctCount++;
                feedbackDiv.innerHTML = `<span class="status-icon">✅</span> <span style="color:#15803d;">Correct! Great match.</span>`;
                inputElement.style.borderColor = "#86efac";
                inputElement.style.backgroundColor = "#f0fdf4";
            } else {
                let expectedDisplay = sentencesData[i].correctAnswer;
                feedbackDiv.innerHTML = `<span class="status-icon">❌</span> <span style="color:#b91c1c;">Wrong. Correct term: <strong>${expectedDisplay}</strong>. Use the word bank.</span>`;
                inputElement.style.borderColor = "#fecaca";
                inputElement.style.backgroundColor = "#fff5f5";
            }
        }
        
        // Update score panel
        const scorePanel = document.getElementById("scorePanel");
        if (correctCount === total) {
            scorePanel.innerHTML = `🎉 PERFECT! SCORE: ${correctCount}/${total} 🎉 All terms used correctly! Excellent work! 🌟`;
            scorePanel.classList.add("perfect-badge");
            scorePanel.style.background = "#d1fae5";
        } else {
            scorePanel.innerHTML = `📊 Your score: ${correctCount} / ${total} correct. ${correctCount === total-1 ? "Almost there!" : "Review the word bank and try again."}`;
            scorePanel.style.background = "#f8f2e3";
            scorePanel.classList.remove("perfect-badge");
        }
    }
    
    // Reset all fields and clear feedback
    function resetAll() {
        for (let i = 0; i < sentenceInputs.length; i++) {
            if (sentenceInputs[i]) {
                sentenceInputs[i].value = "";
                sentenceInputs[i].style.borderColor = "#d6c6a0";
                sentenceInputs[i].style.backgroundColor = "#fffef7";
            }
            const feedbackDiv = document.getElementById(`feedback_${i}`);
            if (feedbackDiv) {
                feedbackDiv.innerHTML = `<span class="status-icon">⏳</span> <span>Not answered yet</span>`;
            }
        }
        document.getElementById("scorePanel").innerHTML = "🔄 Cleared. Fill in the blanks and press 'Check Answers'.";
        document.getElementById("scorePanel").style.background = "#f8f2e3";
        document.getElementById("scorePanel").classList.remove("perfect-badge");
    }
    
    // Add keyboard shortcut (Enter on any field triggers check)
    function bindEnterToCheck() {
        sentenceInputs.forEach(input => {
            if (input) {
                input.removeEventListener("keypress", enterHandler);
                input.addEventListener("keypress", enterHandler);
            }
        });
    }
    
    function enterHandler(e) {
        if (e.key === "Enter") {
            e.preventDefault();
            checkAllAnswers();
        }
    }
    
    // Initialize: render sentences and attach event handlers
    renderSentences();
    // after render, attach events
    document.getElementById("checkBtn").addEventListener("click", checkAllAnswers);
    document.getElementById("resetBtn").addEventListener("click", resetAll);
    
    // Rebind enter after reset or dynamic? reset doesn't change DOM inputs, but we can call after each re-render
    // but renderSentences only once on load. We'll call bind after render.
    setTimeout(() => {
        bindEnterToCheck();
    }, 50);
    
    // also observe if any new inputs appear (not needed but ensure)
    const observer = new MutationObserver(() => {
        bindEnterToCheck();
    });
    observer.observe(document.getElementById("sentencesContainer"), { childList: true, subtree: true });
</script>
</body>
</html>
