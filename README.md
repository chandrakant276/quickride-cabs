<!DOCTYPE html>
<html lang="hi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chandrakant Car Rental</title>
    <style>
        body {
            margin: 0;
            font-family: Arial, sans-serif;
            background: #f4f6f9;
            color: #222;
        }
        header {
            background: #101820;
            color: white;
            text-align: center;
            padding: 25px 10px;
        }
        header h1 {
            color: #ffc107;
            margin-bottom: 8px;
        }
        .hero {
            background: #ffc107;
            text-align: center;
            padding: 35px 15px;
        }
        .hero h2 {
            font-size: 28px;
        }
        .container {
            padding: 20px;
            max-width: 600px;
            margin: auto;
        }
        .card {
            background: white;
            padding: 18px;
            margin: 15px 0;
            border-radius: 12px;
            box-shadow: 0 3px 10px #ddd;
        }
        input, select, button {
            width: 100%;
            padding: 12px;
            margin: 8px 0;
            box-sizing: border-box;
            border-radius: 6px;
            border: 1px solid #ccc;
            font-size: 16px;
        }
        button {
            background: #101820;
            color: white;
            border: none;
            font-weight: bold;
        }
        .whatsapp {
            display: block;
            text-align: center;
            background: #25D366;
            color: white;
            padding: 15px;
            text-decoration: none;
            border-radius: 8px;
            font-weight: bold;
        }
        footer {
            background: #101820;
            color: white;
            text-align: center;
            padding: 20px;
        }
    </style>
</head>
<body>

<header>
    <h1>🚗 CHANDRAKANT CAR RENTAL</h1>
    <p>आपका सफर, हमारी जिम्मेदारी!</p>
    <p>Sonbhadra | Renukoot | Uttar Pradesh</p>
</header>

<section class="hero">
    <h2>Book Your Ride Today!</h2>
    <p>Local • Outstation • Airport • Wedding</p>
    <a href="#booking">
        <button style="background:#101820;">अभी कार बुक करें</button>
    </a>
</section>

<div class="container">

    <div class="card">
        <h2>🚘 हमारी सेवाएँ</h2>
        <p>✅ Local Car Booking</p>
        <p>✅ Outstation Trip</p>
        <p>✅ Airport Pickup & Drop</p>
        <p>✅ Wedding Car Booking</p>
    </div>

    <div class="card" id="booking">
        <h2>📋 कार बुकिंग फॉर्म</h2>

        <form id="bookingForm">
            <input id="name" type="text" placeholder="आपका नाम" required>

            <input id="phone" type="tel"
                   placeholder="आपका मोबाइल नंबर"
                   pattern="[0-9]{10}" required>

            <select id="service" required>
                <option value="">बुकिंग का प्रकार चुनें</option>
                <option>Local</option>
                <option>Outstation</option>
                <option>Airport Pickup & Drop</option>
                <option>Wedding</option>
            </select>

            <input id="pickup" type="text"
                   placeholder="कहाँ से जाना है?" required>

            <input id="drop" type="text"
                   placeholder="कहाँ जाना है?" required>

            <label>यात्रा की तारीख:</label>
            <input id="date" type="date" required>

            <label>पिकअप का समय:</label>
            <input id="time" type="time" required>

            <button type="submit">WhatsApp से बुकिंग भेजें</button>
        </form>
    </div>

    <div class="card">
        <h2>📞 हमसे संपर्क करें</h2>
        <p>मोबाइल: 8853115915</p>
        <a class="whatsapp"
           href="https://wa.me/918853115915"
           target="_blank">
           WhatsApp पर संपर्क करें
        </a>
    </div>

</div>

<footer>
    <p>© 2026 Chandrakant Car Rental</p>
    <p>Renukoot, Sonbhadra, Uttar Pradesh</p>
</footer>

<script>
document.getElementById("bookingForm").addEventListener("submit", function(e) {
    e.preventDefault();

    const name = document.getElementById("name").value;
    const phone = document.getElementById("phone").value;
    const service = document.getElementById("service").value;
    const pickup = document.getElementById("pickup").value;
    const drop = document.getElementById("drop").value;
    const date = document.getElementById("date").value;
    const time = document.getElementById("time").value;

    const message =
        "New Car Booking Request%0A" +
        "Name: " + encodeURIComponent(name) + "%0A" +
        "Customer Mobile: " + encodeURIComponent(phone) + "%0A" +
        "Service: " + encodeURIComponent(service) + "%0A" +
        "Pickup: " + encodeURIComponent(pickup) + "%0A" +
        "Destination: " + encodeURIComponent(drop) + "%0A" +
        "Date: " + encodeURIComponent(date) + "%0A" +
        "Time: " + encodeURIComponent(time);

    window.open("https://wa.me/918853115915?text=" + message, "_blank");
});
</script>

</body>
</html>
