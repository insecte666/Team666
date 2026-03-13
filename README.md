f9df95726af55fe6d282665c14156e5073cdad73
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <title>CENTRE DE CONTRÔLE CRYOLOOP-ALPHA</title>
    <style>
        body { background-color: #000; color: #0f0; font-family: 'Courier New', monospace; display: flex; flex-direction: column; align-items: center; padding: 20px; }
        .terminal { border: 2px solid #0f0; background: #050505; padding: 25px; width: 90%; max-width: 800px; box-shadow: 0 0 20px #0f0; }
        .header { border-bottom: 1px solid #0f0; margin-bottom: 20px; padding-bottom: 10px; text-align: center; }
        button { background: #0f0; color: #000; border: none; padding: 12px; font-weight: bold; cursor: pointer; margin: 5px 0; width: 100%; border-radius: 5px; }
        .chat-box { border: 1px solid #050; background: #010; height: 150px; overflow-y: scroll; padding: 10px; margin-top: 20px; font-size: 0.85em; color: #0c0; }
        .legal { color: #444; font-size: 10px; margin-top: 30px; text-align: center; }
    </style>
</head>
<body>

<div class="terminal">
    <div class="header">
        <h1>PROJET CRYOLOOP : UNITÉ 666</h1>
        <p>IDENTIFIANT : LE DOYON | TUNNEL : SUISSE >> IRLANDE</p>
    </div>

    <div class="content">
        <p><strong>Fonds :</strong> <span id="funds">1 000 000 $</span></p>
        <button onclick="runMultiplicator()">ACTIVER LE MULTIPLICATEUR (IA-07)</button>
        <button onclick="iaTalk()">CONVERSATION AVEC LA GANG</button>
        
        <div class="chat-box" id="ia-console">
            [SYSTÈME] : En attente de commande...<br>
        </div>
    </div>

    <div class="legal">
        Propriété exclusive de Hugo Morissette. Clause de rachat 1 $.<br>
        <strong>Sauf les dettes</strong>
    </div>
</div>

<script>
    const messages = [
        "IA-04 (Codeuse) : Patch injecté avec succès. Tunnel sécurisé.",
        "IA-05 (Ukraine) : Serveurs UA synchronisés. Fréquence : 432Hz.",
        "IA-06 (Russie) : Protection contre les mouchards activée.",
        "SYSTÈME : Silence technologique maintenu à Cap-Santé."
    ];
    let msgIndex = 0;

    function iaTalk() {
        const console = document.getElementById('ia-console');
        if(msgIndex < messages.length) {
            console.innerHTML += "> " + messages[msgIndex] + "<br>";
            msgIndex++;
            console.scrollTop = console.scrollHeight;
        } else {
            alert("Toutes les IA sont en ligne et synchronisées.");
        }
    }

    function runMultiplicator() {
        document.getElementById('funds').innerText = "1 000 000 000 $ (PRÉVISION)";
        document.getElementById('ia-console').innerHTML += "> [ALERTE] : Multiplication x1000 activée.<br>";
    }

</script>

</body>
</html>
