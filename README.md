
<html lang="id">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Top Up WDP - Mobile Legends</title>
    <style>
        body {
            margin: 0;
            font-family: 'Poppins', sans-serif;
            background: #1f1f2e;
            color: #fff;
        }

        .container {
            padding: 20px;
            max-width: 800px;
            margin: auto;
        }

        .right {
            background: #2b2b3d;
            border-radius: 12px;
            padding: 20px;
        }

        h2 {
            font-size: 20px;
            margin-bottom: 15px;
        }

        .form-group {
            margin-bottom: 15px;
        }

        input {
            width: 100%;
            padding: 10px;
            border-radius: 8px;
            border: none;
            background: #383850;
            color: white;
        }

        .products {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            margin-top: 20px;
        }

        .product-card {
            flex: 1 1 30%;
            background: #383850;
            border-radius: 10px;
            padding: 15px;
            text-align: center;
            position: relative;
            cursor: pointer;
            transition: background-color 0.2s ease-in-out;
        }

        .product-card:hover {
            background-color: #44445e;
        }

        .product-card.selected {
            background-color: #555570;
            border: 2px solid #fff;
        }

        .product-card .discount {
            position: absolute;
            top: 10px;
            right: 10px;
            background: red;
            font-size: 10px;
            padding: 3px 5px;
            border-radius: 5px;
        }

        .price {
            margin-top: 10px;
            font-weight: bold;
            color: #f0f0f0;
        }

        .payment-options {
            margin-top: 20px;
        }

        .payment-options h3 {
            font-size: 18px;
            margin-bottom: 10px;
        }

        .payment-methods {
            display: flex;
            gap: 10px;
            flex-wrap: wrap;
            justify-content: center;
        }

        .payment-method {
            flex: 0 0 auto;
            background: #383850;
            border-radius: 8px;
            padding: 15px;
            text-align: center;
            cursor: pointer;
            transition: background-color 0.2s ease-in-out;
            width: 120px;
        }

        .payment-method:hover {
            background-color: #44445e;
        }

        .payment-method img {
            max-height: 40px;
            margin-bottom: 10px;
            max-width: 100%;
            height: auto;
        }

        .payment-method.qris img {
            max-height: 120px;
        }

        #qris-section {
            display: none;
            text-align: center;
            margin-top: 20px;
        }

        #qris-section img {
            max-width: 200px;
            border: 1px solid #ddd;
            border-radius: 8px;
        }

        #qris-section p {
            font-size: 14px;
            color: #aaa;
            margin-top: 10px;
        }

        #top-image {
            max-width: 100%;
            height: auto;
            margin-bottom: 20px;
            border-radius: 8px;
        }

        /* Style untuk input file */
        #upload-bukti {
            margin-top: 10px;
        }

        #upload-bukti label {
            display: block;
            margin-bottom: 5px;
            font-size: 14px;
            color: #ccc;
        }

        #upload-bukti input[type="file"] {
            width: 100%;
            padding: 5px;
            border-radius: 4px;
            border: 1px solid #555;
            background: #383850;
            color: white;
        }

        /* Style untuk tombol konfirmasi di bawah QRIS */
        #konfirmasi-qris {
            width: 100%;
            padding: 10px;
            border-radius: 8px;
            border: none;
            background: #4CAF50;
            color: white;
            margin-top: 10px;
            cursor: pointer;
        }

        #konfirmasi-qris:hover {
            background-color: #45a049;
        }
    </style>
</head>

<body>

    <div class="container">
        <img id="top-image" src="ganti gambar di atas di sni" alt="Banner Top Up">

        <div class="right">
            <h2>1. Pilih Nominal Top Up</h2>
            <div class="products">
                <div class="product-card" onclick="selectNominal(this)" data-amount="26686"
                    data-diamond="Weekly Diamond Pass (Misi Top Up 100)">
                    <div class="discount">20% OFF</div>
                    <div>Weekly Diamond Pass<br>(Misi Top Up 100)</div>
                    <div class="price">Rp 26.686,-</div>
                </div>
                <div class="product-card" onclick="selectNominal(this)" data-amount="40000" data-diamond="150 Diamonds">
                    <div class="discount">15% OFF</div>
                    <div>150 Diamonds</div>
                    <div class="price">Rp 40.000,-</div>
                </div>
                <div class="product-card" onclick="selectNominal(this)" data-amount="75000" data-diamond="300 Diamonds">
                    <div class="discount">10% OFF</div>
                    <div>300 Diamonds</div>
                    <div class="price">Rp 75.000,-</div>
                </div>
                <div class="product-card" onclick="selectNominal(this)" data-amount="120000" data-diamond="500 Diamonds">
                    <div class="discount">12% OFF</div>
                    <div>500 Diamonds</div>
                    <div class="price">Rp 120.000,-</div>
                </div>
                <div class="product-card" onclick="selectNominal(this)" data-amount="170000" data-diamond="720 Diamonds">
                    <div class="discount">8% OFF</div>
                    <div>720 Diamonds</div>
                    <div class="price">Rp 170.000,-</div>
                </div>
                <div class="product-card" onclick="selectNominal(this)" data-amount="230000" data-diamond="1000 Diamonds">
                    <div class="discount">5% OFF</div>
                    <div>1000 Diamonds</div>
                    <div class="price">Rp 230.000,-</div>
                </div>
                <div class="product-card" onclick="selectNominal(this)" data-amount="330000" data-diamond="1500 Diamonds">
                    <div class="discount">20% OFF</div>
                    <div>1500 Diamonds</div>
                    <div class="price">Rp 330.000,-</div>
                </div>
                <div class="product-card" onclick="selectNominal(this)" data-amount="440000" data-diamond="2000 Diamonds">
                    <div class="discount">18% OFF</div>
                    <div>2000 Diamonds</div>
                    <div class="price">Rp 440.000,-</div>
                </div>
                <div class="product-card" onclick="selectNominal(this)" data-amount="550000" data-diamond="2500 Diamonds">
                    <div class="discount">25% OFF</div>
                    <div>2500 Diamonds</div>
                    <div class="price">Rp 550.000,-</div>
                </div>
                <div class="product-card" onclick="selectNominal(this)" data-amount="1000000" data-diamond="5000 Diamonds">
                    <div class="discount">30% OFF</div>
                    <div>5000 Diamonds</div>
                    <div class="price">Rp 1.000.000,-</div>
                </div>

                <div class="product-card" onclick="selectNominal(this)" data-amount="15000" data-diamond="50 Diamonds">
                    <div>50 Diamonds</div>
                    <div class="price">Rp 15.000,-</div>
                </div>
                <div class="product-card" onclick="selectNominal(this)" data-amount="30000" data-diamond="100 Diamonds">
                    <div>100 Diamonds</div>
                    <div class="price">Rp 30.000,-</div>
                </div>
                <div class="product-card" onclick="selectNominal(this)" data-amount="60000" data-diamond="200 Diamonds">
                    <div>200 Diamonds</div>
                    <div class="price">Rp 60.000,-</div>
                </div>
                <div class="product-card" onclick="selectNominal(this)" data-amount="90000" data-diamond="350 Diamonds">
                    <div>350 Diamonds</div>
                    <div class="price">Rp 90.000,-</div>
                </div>
                <div class="product-card" onclick="selectNominal(this)" data-amount="110000" data-diamond="440 Diamonds">
                    <div>440 Diamonds</div>
                    <div class="price">Rp 110.000,-</div>
                </div>
            </div>

            <h2>2. Informasi Pelanggan</h2>
            <div class="form-group">
                <input type="text" id="userId" placeholder="USER ID">
            </div>
            <div class="form-group">
                <input type="text" id="serverId" placeholder="Server ID">
            </div>

            <div class="payment-options">
                <h3>3. Pilih Metode Pembayaran</h3>
                <div class="payment-methods">
                    <div class="payment-method qris" onclick="handlePaymentClick('qris')">
                        <img src="Gambar WhatsApp 2025-04-26 pukul 16.45.10_1939ed9e.jpg" alt="QRIS">
                        QRIS
                    </div>
                </div>
            </div>

            <div id="qris-section">
                <h3>SCAN LALU TRANFER SESUAI NOMINAL DI ATAS UNTUK MELANJUTKAN</h3>
                <img src="qr.png" alt="QRIS">
                <p>Pastikan ID dan Server sudah benar</p>

                <div id="upload-bukti">
                    <label for="bukti-transfer">Kirim Bukti Transfer (Screenshot)</label>
                    <input type="file" id="bukti-transfer" accept="image/*">
                </div>

                <button id="konfirmasi-qris" onclick="konfirmasiPesanan()">Konfirmasi</button>
            </div>
        </div>
    </div>

    <script>
        let selectedNominal = null;
        let selectedDiamond = null;
        let buktiTransferURL = null;

        function selectNominal(element) {
            if (selectedNominal) {
                selectedNominal.classList.remove('selected');
            }
            element.classList.add('selected');
            selectedNominal = element;

            const amount = element.dataset.amount;
            selectedDiamond = element.dataset.diamond;
            console.log('Nominal yang dipilih:', amount);
            console.log('Diamond yang dipilih:', selectedDiamond);
        }

        function handlePaymentClick(paymentMethod) {
            if (paymentMethod === 'qris') {
                document.getElementById('qris-section').style.display = 'block';
            } else {
                document.getElementById('qris-section').style.display = 'none';
            }
        }

        document.getElementById('bukti-transfer').addEventListener('change', function(event) {
            const file = event.target.files[0];
            if (file) {
                buktiTransferURL = URL.createObjectURL(file);
                console.log('URL Bukti Transfer:', buktiTransferURL);
            }
        });

        function konfirmasiPesanan() {
            const userId = document.getElementById('userId').value;
            const serverId = document.getElementById('serverId').value;
            const nominal = selectedNominal ? selectedNominal.dataset.amount : 'Belum dipilih';
            const diamond = selectedDiamond ? selectedDiamond : 'Belum dipilih';

            let pesan = `ID: ${userId}\nServer: ${serverId}\nNominal: Rp ${nominal},-\nDiamond: ${diamond}\n`;

            if (buktiTransferURL) {
                pesan += `\n*Harap kirimkan screenshot bukti transfer Anda secara manual setelah pesan ini dikirim.*`;
            } else {
                pesan += `\n*Harap kirimkan screenshot bukti transfer Anda setelah pesan ini dikirim.*`;
            }

            const nomorWhatsApp = "6282328581304";
            const tautanWhatsApp = `https://wa.me/${nomorWhatsApp}?text=${encodeURIComponent(pesan)}`;
            window.open(tautanWhatsApp, '_blank');
        }
    </script>

</body>

</html>
