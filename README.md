<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Energy Demand Calculations</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            margin: 0;
            padding: 0;
            color: #333;
        }
        header {
            background-color: #005f73;
            color: white;
            text-align: center;
            padding: 1.5em 0;
        }
        h1 {
            font-size: 2.5em;
            margin: 0;
        }
        section {
            padding: 2em;
        }
        .content {
            background-color: white;
            border-radius: 8px;
            padding: 2em;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            margin-bottom: 2em;
        }
        .content h2 {
            color: #0077b6;
        }
        .content p {
            line-height: 1.6;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 1em;
        }
        table, th, td {
            border: 1px solid #ddd;
        }
        th, td {
            padding: 12px;
            text-align: left;
        }
        th {
            background-color: #0077b6;
            color: white;
        }
        .footer {
            background-color: #333;
            color: white;
            text-align: center;
            padding: 1em;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    </style>
</head>
<body>

<header>
    <h1>Energy Demand Calculations</h1>
</header>

<section>
    <div class="content">
        <h2>a) Energy Demand in France</h2>

        <h3>1. Energy Demand in the Year 2000</h3>
        <p>To calculate the energy demand in the year 2000, given that the growth rate from 2000 to 2015 is 3.6%, we use the compound growth formula:</p>
        <p><em>P<sub>t</sub> = P<sub>0</sub> × (1 + r)<sup>t</sup></em></p>
        <p>Where:</p>
        <ul>
            <li>P<sub>t</sub> is the value in 2015 (5720 Mtoe)</li>
            <li>P<sub>0</sub> is the value in 2000 (which we need to find)</li>
            <li>r is the growth rate (3.6% or 0.036)</li>
            <li>t is the time period (15 years, from 2000 to 2015)</li>
        </ul>
        <p>Substituting the values, we get:</p>
        <p><em>P<sub>0</sub> = 5720 / (1 + 0.036)<sup>15</sup> = 3310.57 Mtoe</em></p>
        <p>The energy demand in 2000 is approximately 3310.57 Mtoe.</p>

        <h3>2. Growth Rate Between 2015 and 2016</h3>
        <p>The growth rate between 2015 and 2016 is calculated using the formula:</p>
        <p><em>Growth Rate = (P<sub>2016</sub> - P<sub>2015</sub>) / P<sub>2015</sub> × 100</em></p>
        <p>Where:</p>
        <ul>
            <li>P<sub>2015</sub> = 5720 Mtoe</li>
            <li>P<sub>2016</sub> = 5970 Mtoe</li>
        </ul>
        <p>The growth rate is approximately 4.37%.</p>
    </div>

    <div class="content">
        <h2>b) Energy Demand in Germany</h2>

        <h3>1. Primary Energy Consumption in 2015</h3>
        <p>The GDP elasticity of energy demand formula is:</p>
        <p><em>Energy Demand Growth = GDP Growth × Elasticity</em></p>
        <p>Where:</p>
        <ul>
            <li>Elasticity = 2.4</li>
            <li>GDP in 2015 = 23 billion Euro</li>
            <li>GDP in 2016 = 24.5 billion Euro</li>
        </ul>
        <p>The GDP growth rate is calculated as 6.52%, and the energy demand growth is 15.65%. Using this, we calculate the primary energy consumption in 2015:</p>
        <p><em>P<sub>2015</sub> = 1300 × (1 + 0.1565) = 1123.52 Mtoe</em></p>
        <p>The primary energy consumption in Germany in 2015 is approximately 1123.52 Mtoe.</p>
    </div>

    <div class="content">
        <h2>c) Forecast of Jordan's Primary Energy Consumption (2010-2017)</h2>
        <p>Using linear regression based on the data from 2001 to 2010, the forecasted primary energy consumption for Jordan from 2011 to 2017 is as follows:</p>

        <table>
            <tr>
                <th>Year</th>
                <th>Forecasted Energy Consumption (Mtoe)</th>
            </tr>
            <tr>
                <td>2011</td>
                <td>6200</td>
            </tr>
            <tr>
                <td>2012</td>
                <td>6500</td>
            </tr>
            <tr>
                <td>2013</td>
                <td>6800</td>
            </tr>
            <tr>
                <td>2014</td>
                <td>7100</td>
            </tr>
            <tr>
                <td>2015</td>
                <td>7400</td>
            </tr>
            <tr>
                <td>2016</td>
                <td>7700</td>
            </tr>
            <tr>
                <td>2017</td>
                <td>8000</td>
            </tr>
        </table>

        <p>These values are estimated using linear regression based on historical data from 2001 to 2010.</p>
    </div>
</section>

<div class="footer">
    <p>&copy; 2024 Energy Demand Calculations - All Rights Reserved</p>
</div>

</body>
</html>
