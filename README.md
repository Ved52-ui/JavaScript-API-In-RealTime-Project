# 🚚 JavaScript-API-In-RealTime-Project

🔗 **Live Demo**: [Click Here to Track Your Consignment](https://www.rishabhroadlines.in/track.html)  
💡 Try this Tracking ID: `AHD00001`
---
idshshshsjdh62-₹
## 📌 Project Overview

This project demonstrates **how to fetch and display real-time API data using JavaScript** — perfect for tracking systems, live dashboards, or dynamic content applications.

It is a part of the [Rishabh Roadlines](https://www.rishabhroadlines.in/) live freight tracking website, where users can enter their consignment number and see the delivery progress **instantly**.


## 🎯 Features

- ✅ Fetch API using `POST` method with custom data
- ✅ Handle JSON responses dynamically
- ✅ Clean error handling for user-friendly messages
- ✅ Live progress UI update
- ✅ Deployed and functional in real-time!

---

## 💻 How To Use The Code

Here’s the **magic JavaScript snippet** used to call the API and show data in real-time:

```javascript
fetch("Your API URL Or File", {
  method: "POST",
  headers: {
    "Content-Type": "application/json"
  },
  body: JSON.stringify({ sqry: Data }) // Replace 'Data' with your actual input
})
.then((response) => response.json())
.then((response) => {
  console.log(response); // For debugging in console
  if (Array.isArray(response) && response.length > 0) {
    progress.innerHTML = yourfunction(response); // Your custom rendering logic
  } else {
    progress.innerHTML = `<p style="color:red;">No data found for this.</p>`;
  }
})
.catch(err => {
  console.error(err);
  progress.innerHTML = `<p style="color:red;">Error fetching data. Please try again later.</p>`;
});
