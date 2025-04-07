# MyHealthConnect: Real-Time Patient Data Viewer

This is a web-based application that provides a real-time view of patient health data fetched from a SMART Health IT FHIR API. It displays patient information, medications, and conditions in a user-friendly and engaging interface.

## Features

* **Real-Time Data:** Fetches and updates patient data periodically (every 10 seconds by default).
* **Patient Information:** Displays the patient's name.
* **Medications:** Lists the patient's current medications with relevant icons.
* **Conditions:** Lists the patient's current health conditions with relevant icons.
* **Modern UI:** Utilizes the Bootstrap 5 framework with the visually appealing "Lux" theme from Bootswatch for a polished look.
* **Engaging Visuals:** Incorporates Font Awesome icons to enhance the presentation of data.
* **Loading and Error Handling:** Provides visual feedback during data loading and displays informative error messages if issues occur.
* **Optional Patient Selection:** Includes a basic dropdown to select different patient IDs (easily expandable).

## Technologies Used

* **HTML:** For the structure of the web page.
* **CSS:** Primarily handled by Bootstrap 5 and the "Lux" theme for styling. Custom styles are included for specific elements.
* **JavaScript:** For fetching data from the FHIR API, dynamically updating the HTML, handling loading states, and providing basic interactivity.
* **Bootstrap 5:** A popular CSS framework for responsive and modern design.
* **Bootswatch (Lux Theme):** A set of free themes for Bootstrap, providing a distinct visual style.
* **Font Awesome:** A comprehensive icon library used for visual representation of data.

## Setup and Usage

1.  **Clone the Repository (if applicable):** If this project is hosted on GitHub, clone the repository to your local machine:
    ```bash
    git clone <repository_url>
    cd myhealthconnect
    ```

2.  **Open the HTML file:** Simply open the `index.html` (or the name of your HTML file) in your web browser.

3.  **View the Data:** The application will automatically start fetching and displaying data for the default patient (`smart-1032702`).

4.  **(Optional) Select a Different Patient:** If the patient selection dropdown has more options, you can choose a different patient ID and click the "Load Data" button to view their information.

## Configuration

* **`BASE_URL`:** This constant in the JavaScript code (`const BASE_URL = 'https://r4.smarthealthit.org';`) defines the base URL of the FHIR API endpoint. You might need to adjust this if you are using a different FHIR server.
* **`PATIENT_ID`:** The `currentPatientId` variable (initialized to `'smart-1032702'`) determines the default patient whose data is fetched. You can change this directly in the JavaScript code or use the patient selection dropdown in the UI.
* **Update Interval:** The `setInterval(loadPatientData, 10000);` line sets the data refresh interval to 10000 milliseconds (10 seconds). You can modify this value to control how frequently the data is updated.
* **Icons:** The `getMedicationIcon` and `getConditionIcon` functions determine which Font Awesome icons are displayed for medications and conditions based on their names. You can customize the logic within these functions to use different icons or add more specific mappings.
* **Bootswatch Theme:** The "Lux" theme is currently linked in the `<head>`. To use a different Bootswatch theme, modify the `href` attribute of the CSS link to the desired theme's CDN URL (as described on [https://bootswatch.com/](https://bootswatch.com/)).

## Potential Enhancements

* **More Detailed Information:** Display additional details about medications and conditions (e.g., dosage, severity).
* **Data Visualization:** Implement charts or graphs for numerical health data (if available in the FHIR API).
* **User Authentication:** Add user authentication to securely access patient data.
* **Filtering and Sorting:** Allow users to filter and sort the lists of medications and conditions.
* **More Interactive Elements:** Implement features like tooltips on hover or expandable sections for more information.
* **Theming Options:** Provide a user interface to switch between different Bootswatch themes.
* **Responsive Design Improvements:** Further refine the layout for different screen sizes.

## Disclaimer

This application is for demonstration purposes and uses a public SMART Health IT FHIR API endpoint with sample data. It should not be used for real clinical decision-making. Always consult with qualified healthcare professionals for medical advice.

## License

[Specify your project license here, e.g., MIT License]
