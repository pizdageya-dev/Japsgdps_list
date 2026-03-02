# Japsgdps_list
Demon,pemon and challenge list's 
<!DOCTYPE html><html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Demon List Site</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background-color: #111;
            color: white;
        }.tabs {
        display: flex;
        background-color: #000;
        border-bottom: 3px solid orange;
    }

    .tab-button {
        flex: 1;
        padding: 15px;
        background: none;
        border: none;
        color: orange;
        cursor: pointer;
        font-size: 16px;
        font-weight: bold;
        transition: 0.3s;
    }

    .tab-button:hover {
        background-color: orange;
        color: black;
    }

    .tab-button.active {
        background-color: orange;
        color: black;
    }

    .tab-content {
        display: none;
        padding: 30px;
    }

    .tab-content.active {
        display: block;
    }

    .level {
        background-color: #1a1a1a;
        padding: 15px;
        margin: 10px 0;
        border-left: 5px solid orange;
        transition: 0.3s;
    }

    .level:hover {
        background-color: #222;
        transform: translateX(5px);
    }

    h2 {
        color: orange;
    }
</style>

</head>
<body><div class="tabs">
    <button class="tab-button active" onclick="openTab('demon')">Demon List</button>
    <button class="tab-button" onclick="openTab('pemon')">Pemon List</button>
    <button class="tab-button" onclick="openTab('challenge')">Challenge List</button>
</div>

<div id="demon" class="tab-content active">
    <h2>Demon List</h2>
    <div class="level">1. Inferno Blade</div>
    <div class="level">2. Dark Abyss</div>
    <div class="level">3. Shadow Core</div>
    <div class="level">4. Hell Storm</div>
    <div class="level">5. Crimson Wave</div>
    <div class="level">6. Night Terror</div>
    <div class="level">7. Chaos Machine</div>
    <div class="level">8. Flame Rift</div>
    <div class="level">9. Black Impact</div>
    <div class="level">10. Void Collapse</div>
</div>

<div id="pemon" class="tab-content">
    <h2>Pemon List</h2>
    <div class="level">1. Orange Pulse</div>
    <div class="level">2. Cyber Rush</div>
    <div class="level">3. Plasma Run</div>
    <div class="level">4. Neon Strike</div>
    <div class="level">5. Speed Vortex</div>
    <div class="level">6. Toxic Dash</div>
    <div class="level">7. Rapid Wave</div>
    <div class="level">8. Flash Reactor</div>
    <div class="level">9. Power Grid</div>
    <div class="level">10. Storm Dash</div>
</div>

<div id="challenge" class="tab-content">
    <h2>Challenge List</h2>
    <div class="level">1. Mini Wave Spam</div>
    <div class="level">2. Straight Fly 100%</div>
    <div class="level">3. Invisible Blocks</div>
    <div class="level">4. Speed Trial</div>
    <div class="level">5. Tight Corridor</div>
    <div class="level">6. Double Click Timing</div>
    <div class="level">7. Micro Cube</div>
    <div class="level">8. Memory Path</div>
    <div class="level">9. Gravity Chaos</div>
    <div class="level">10. Final Reaction</div>
</div>

<script>
    function openTab(tabId) {
        const buttons = document.querySelectorAll('.tab-button');
        const contents = document.querySelectorAll('.tab-content');

        buttons.forEach(btn => btn.classList.remove('active'));
        contents.forEach(content => content.classList.remove('active'));

        document.getElementById(tabId).classList.add('active');
        event.currentTarget.classList.add('active');
    }
</script>

</body>
</html>
