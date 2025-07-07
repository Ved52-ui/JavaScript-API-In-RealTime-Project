# JavaScript-API-In-RealTime-Project
https://www.rishabhroadlines.in/track.html
### This WebSite Is Made By Me Click The link And Check The Output Enter The Tracking Number e.g AHD00001
# How To Fetch Api In Javascript
### This Is A Perfect Code To Add Any Api In Javascript  
### This Code Is For Getting Data In JSON Format
    fetch("Your API URL Or File", {
      method: "POST",
      headers: {
        "Content-Type": "application/json"
      },
      body: JSON.stringify({ sqry: Data })
    })
    
    .then((response) => response.json())
    .then((response) => {
      console.log(response); // for debugging
      if (Array.isArray(response) && response.length > 0) {
        progress.innerHTML = yourfunction(response);
      } else {
        progress.innerHTML = `<p style="color:red;">No data found for this .</p>`;
      }
    })
    .catch(err => {
      console.error(err);
      progress.innerHTML = `<p style="color:red;">Error fetching data. Please try again later.</p>`;
    });
