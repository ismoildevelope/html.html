<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>XAU/USD Candlestick Chart</title>
    <!-- Plotly JS kutubxonasini ulash -->
    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
</head>
<body>

    <h2>XAU/USD (Oltin) 15m Candlestick Chart</h2>

    <!-- Candlestick grafikni joylashtiradigan joy -->
    <div id="chart"></div>

    <script>
        // XAU/USD (Oltin) ma'lumotlarini qo'lda yaratish
        var data = [{
            type: 'candlestick',
            x: [
                '2025-05-01 00:00:00', '2025-05-01 00:15:00', '2025-05-01 00:30:00', // Xarita va vaqt
                '2025-05-01 00:45:00', '2025-05-01 01:00:00'
            ],
            open: [1800, 1801, 1805, 1810, 1812],   // Ochiq narxlar
            high: [1812, 1815, 1820, 1823, 1825],   // Yuksalish narxlari
            low: [1798, 1800, 1802, 1805, 1808],    // Past narxlar
            close: [1805, 1810, 1812, 1815, 1820],  // Yopilish narxlari
        }];

        var layout = {
            title: 'XAU/USD Candlestick Chart',
            xaxis: {
                rangeslider: {
                    visible: false
                }
            },
            yaxis: {
                title: 'Price in USD'
            }
        };

        // Grafikni yaratish
        Plotly.newPlot('chart', data, layout);
    </script>

</body>
</html>
