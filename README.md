<!DOCTYPE html>
<html lang="hi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>QuickRide Cabs | Online Car Booking</title>

<style>
* {
    box-sizing: border-box;
}

body {
    margin: 0;
    font-family: Arial, sans-serif;
    background: #f3f5f9;
    color: #172033;
}

header {
    background: #101827;
    color: white;
    padding: 22px 15px;
    text-align: center;
}

header h1 {
    color: #ffc107;
    margin: 0;
}

header p {
    margin-bottom: 0;
}

.hero {
    background: #ffc107;
    padding: 35px 15px;
    text-align: center;
}

.hero h2 {
    font-size: 28px;
    margin-top: 0;
}

.container {
    max-width: 850px;
    margin: auto;
    padding: 15px;
}

.card {
    background: white;
    padding: 20px;
    margin: 18px 0;
    border-radius: 12px;
    box-shadow: 0 3px 12px #00000010;
}

.car {
    border: 1px solid #ddd;
    padding: 15px;
    border-radius: 10px;
    margin: 12px 0;
}

.car h3 {
    margin-top: 0;
}

.status {
    color: #16803c;
    font-weight: bold;
}

label {
    display: block;
    margin-top: 12px;
    font-weight: bold;
}

input, select, button {
    width: 100%;
    padding: 13px;
    margin-top: 7px;
    border: 1px solid #ccd2dc;
    border-radius: 7px;
    font-size: 16px;
}

button {
    background: #101827;
    color: white;
    border: none;
    cursor: pointer;
    font-weight: bold;
}

button:disabled {
    background: #777;
}

.contact {
    background: #101827;
    color: white;
    text-align: center;
    padding: 25px 15px;
}

.call {
    display: inline-block;
    padding: 13px 25px;
    background: #ffc107;
    color: #101827;
    text-decoration: none;
    border-radius: 7px;
    font-weight: bold;
}

footer {
    text-align: center;
    padding: 15px;
}
</style>
</head>

<body>

<header>
    <h1>🚗 QuickRide Cabs</h1>
    <p>आपका सफर, हमारी जिम्मेदारी!</p>
    <p>Local • Outstation • Airport • Wedding</p>
</header>

<section class="hero">
    <h2>Book Your Ride</h2>
    <p>अपनी पसंद की कार चुनें और बुकिंग रिक्वेस्ट भेजें।</p>
</section>

<main class="container">

    <section class="card">
        <h2>🚘 हमारी कारें</h2>
        <p>नीचे अपनी पसंद की कार चुनें। उपलब्धता की वास्तविक जानकारी ऑनलाइन डेटाबेस जुड़ने के बाद दिखाई जाएगी।</p>

        <div id="carList">
            <div class="car">
                <h3>Maruti Suzuki Dzire</h3>
                <p>सेडान • 4 यात्री</p>
                <p>किराया: मालिक से पूछें</p>
                <p class="status">उपलब्धता की पुष्टि जरूरी</p>
            </div>

            <div class="car">
                <h3>Maruti Suzuki Ertiga</h3>
                <p>फैमिली कार • 6–7 यात्री</p>
                <p>किराया: मालिक से पूछें</p>
                <p class="status">उपलब्धता की पुष्टि जरूरी</p>
            </div>

            <div class="car">
                <h3>Toyota Innova Crysta</h3>
                <p>प्रीमियम कार</p>
                <p>किराया: मालिक से पूछें</p>
                <p class="status">उपलब्धता की पुष्टि जरूरी</p>
            </div>
        </div>
    </section>

    <section class="card" id="booking">
        <h2>📋 ऑनलाइन बुकिंग रिक्वेस्ट</h2>

        <form id="bookingForm">

            <label for="customer">आपका नाम</label>
            <input id="customer" required maxlength="80">

            <label for="phone">मोबाइल नंबर</label>
            <input id="phone" type="tel"
                   pattern="[0-9]{10}" maxlength="10"
                   placeholder="10 अंकों का मोबाइल नंबर" required>

            <label for="service">बुकिंग का प्रकार</label>
            <select id="service" required>
                <option value="">चुनें</option>
                <option>Local</option>
                <option>Outstation</option>
                <option>Airport Pickup & Drop</option>
                <option>Wedding</option>
            </select>

            <label for="car">अपनी कार चुनें</label>
            <select id="car" required>
                <option value="">कार चुनें</option>
                <option>Maruti Suzuki Dzire</option>
                <option>Maruti Suzuki Ertiga</option>
                <option>Toyota Innova Crysta</option>
            </select>

            <label for="pickup">पिकअप की जगह</label>
            <input id="pickup" required maxlength="200">

            <label for="destination">कहाँ जाना है?</label>
            <input id="destination" required maxlength="200">

            <label for="date">यात्रा की तारीख</label>
            <input id="date" type="date" required>

            <label for="time">पिकअप का समय</label>
            <input id="time" type="time" required>

            <button type="submit">बुकिंग रिक्वेस्ट तैयार करें</button>
        </form>

        <p id="message" role="status"></p>
    </section>

    <section class="card">
        <h2>📍 बुक की गई कार की लाइव लोकेशन</h2>
        <p>बुकिंग कन्फर्म होने और ड्राइवर द्वारा GPS लोकेशन शेयर करने की सुविधा जुड़ने के बाद यहाँ लाइव ट्रैकिंग उपलब्ध होगी।</p>
        <p>अभी लाइव लोकेशन उपलब्ध नहीं है।</p>
    </section>

</main>

<section class="contact">
    <h2>QuickRide Cabs</h2>
    <p>बुकिंग और जानकारी के लिए संपर्क करें।</p>
    <a class="call" href="tel:8853115915">📞 8853115915 पर कॉल करें</a>
</section>

<footer>
    © 2026 QuickRide Cabs
</footer>

<script>
document.getElementById("bookingForm").addEventListener("submit", function(event) {
    event.preventDefault();

    const booking = {
        customer: document.getElementById("customer").value.trim(),
        phone: document.getElementById("phone").value.trim(),
        service: document.getElementById("service").value,
        car: document.getElementById("car").value,
        pickup: document.getElementById("pickup").value.trim(),
        destination: document.getElementById("destination").value.trim(),
        date: document.getElementById("date").value,
        time: document.getElementById("time").value
    };

    const message = document.getElementById("message");

    if (!/^[0-9]{10}$/.test(booking.phone)) {
        message.textContent = "कृपया सही 10 अंकों का मोबाइल नंबर भरें।";
        return;
    }

    message.textContent =
        "आपकी जानकारी तैयार है, लेकिन ऑनलाइन बुकिंग अभी सक्रिय नहीं है। " +
        "बुकिंग रिक्वेस्ट भेजने के लिए डेटाबेस और सुरक्षित सर्वर जोड़ना बाकी है।";
});
</script>

</body>
</html>
