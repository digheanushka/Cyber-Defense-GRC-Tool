# Cyber-Defense-GRC-Tool
A web-based Cyber Defence GRC (Governance, Risk and Compliance) tool for managing assets, identifying cybersecurity risks, calculating risk scores, and monitoring security posture through a simple dashboard.

<!DOCTYPE html>
<html>
<head>
    <title>Cyber Defence GRC Tool</title>
    <link rel="stylesheet" href="style.css">
</head>

<body>

    <header>
        <h1>Cyber Defence GRC Tool</h1>
        <p>Governance, Risk and Compliance Dashboard</p>
    </header>

    <nav>
        <button onclick="showPage('dashboard')">Dashboard</button>
        <button onclick="showPage('assets')">Assets</button>
        <button onclick="showPage('risks')">Risks</button>
    </nav>

    <main>

        <!-- Dashboard -->

        <section id="dashboard">

            <h2>Dashboard</h2>

            <div class="cards">

                <div class="card">
                    <h3>Total Assets</h3>
                    <p id="assetCount">0</p>
                </div>

                <div class="card">
                    <h3>Total Risks</h3>
                    <p id="riskCount">0</p>
                </div>

                <div class="card danger">
                    <h3>High Risks</h3>
                    <p id="highRiskCount">0</p>
                </div>

            </div>

        </section>


        <!-- Assets -->

        <section id="assets" class="hidden">

            <h2>Asset Management</h2>

            <input
                type="text"
                id="assetName"
                placeholder="Enter asset name">

            <input
                type="text"
                id="assetType"
                placeholder="Enter asset type">

            <button onclick="addAsset()">
                Add Asset
            </button>

            <h3>Asset List</h3>

            <table>

                <thead>
                    <tr>
                        <th>Asset</th>
                        <th>Type</th>
                    </tr>
                </thead>

                <tbody id="assetTable"></tbody>

            </table>

        </section>


        <!-- Risks -->

        <section id="risks" class="hidden">

            <h2>Risk Management</h2>

            <input
                type="text"
                id="riskName"
                placeholder="Enter risk">

            <label>Likelihood (1-5)</label>

            <input
                type="number"
                id="likelihood"
                min="1"
                max="5">

            <label>Impact (1-5)</label>

            <input
                type="number"
                id="impact"
                min="1"
                max="5">

            <button onclick="addRisk()">
                Calculate Risk
            </button>

            <h3>Risk List</h3>

            <table>

                <thead>
                    <tr>
                        <th>Risk</th>
                        <th>Likelihood</th>
                        <th>Impact</th>
                        <th>Score</th>
                        <th>Level</th>
                    </tr>
                </thead>

                <tbody id="riskTable"></tbody>

            </table>

        </section>

    </main>

    <script src="script.js"></script>

</body>
</html>

