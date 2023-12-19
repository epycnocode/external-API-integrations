# Webflow Goes Global: External APIs for Real-Time Magic

Think of your Webflow site as a superhero. But what if it could tap into the powers of other heroes through APIs? That's where external API integrations come in, injecting real-time data and powerful functionalities to make your website truly superhuman. Here's a quick rundown with code examples that'll make you feel like a coding wizard (without the spells):

**1. API Superpowers:**

  - **Live Data:** Imagine a weather website that updates with real-time conditions, or a travel site showing live flight prices. APIs make it possible!
  - **Customizable Functionalities:** Need a booking system or a dynamic quiz? APIs can unlock a world of possibilities beyond what Webflow offers natively.
  - **Global Connections:** Tap into data and services from all over the internet, enriching your website and reaching a wider audience.

**2. Code Examples without the Kryptonite:**

**Example 1: Displaying live weather data:**

  1. Choose a weather API like OpenWeatherMap.
  2. Use Webflow's "API request" element to fetch the data for your location.
```
HTMl
<wf-api-request
  url="https://api.openweathermap.org/data/2.5/weather?q=London&appid=YOUR_API_KEY"
  method="GET"
  on-success="updateWeatherData"
></wf-api-request>

```
  3. Write a simple JavaScript function to update your UI with the received data.
```
JavaScript
function updateWeatherData(data) {
  document.getElementById("temperature").textContent = data.main.temp;
  document.getElementById("description").textContent = data.weather[0].description;
}

```

**Example 2: Triggering a booking form when a user selects a date:**

  1. Integrate with a booking platform API.
  2. Use Webflow Interactions to capture the date selection from a calendar.
```
HTMl
<wf-interaction
  for="date-picker"
  on-change="triggerBookingForm"
></wf-interaction>

```
  3. Write a JavaScript function to send the selected date to the booking API and display the form.
```
JavaScript
function triggerBookingForm(event) {
  const selectedDate = event.detail.value;
  fetchBookingAvailability(selectedDate); // Call your booking API
  document.getElementById("booking-form").style.display = "block";
}

```
# Need Help?
Want to build a [custom webflow page](https://epyc.in/)?
