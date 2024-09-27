# FOOD-INTAKE-TRACKER-AND-HEALTH-ADVISOR-LIM-LARGE-IMAGE-MODEL-APP

This is a **Health Advisor** app that allows users to upload images of food items and receive an analysis of the total calorie content. It uses **Google Gemini Pro Vision API** to recognize food items and provide details on calories, nutrition breakdown, and whether the food is healthy or not.

---

## Features

- **Image Upload**: Upload images of food in `.jpg`, `.jpeg`, or `.png` format.
- **Nutrition and Calorie Calculation**: The app identifies the food items in the image, calculates the total calories, and provides a detailed breakdown for each item.
- **Health Analysis**: Provides a report on whether the meal is healthy or not, along with the percentage breakdown of carbohydrates, fats, fiber, sugar, and other essential nutrients.

---

## Prerequisites

- Python 3.7+
- **Streamlit**: For building the web app interface.
- **Google Gemini Pro Vision API**: For image processing and food recognition.
- **PIL**: To handle and display images.
- **dotenv**: To load environment variables, such as your Google API key.

---

## Installation

1. **Clone the repository:**
    ```bash
    git clone [https://github.com/hariharanrb7/FOOD-CALORIES-TRACKING-WEBAPP]
    ```

2. **Install the required libraries:**
    ```bash
    pip install streamlit google-generativeai python-dotenv Pillow
    ```

3. **Set up your environment variables:**
   - Create a `.env` file in the root directory.
   - Add your **Google API Key** to the `.env` file:
     ```
     GOOGLE_API_KEY=your_google_api_key_here
     ```

---

## Usage

1. **Run the Streamlit app:**
    ```bash
    streamlit run app.py
    ```

2. **Upload an Image**: On the app interface, click on "Choose an image..." to upload an image of food in `.jpg`, `.jpeg`, or `.png` format.

3. **Submit for Analysis**: Click the "Tell me the total calories" button to get the nutritional analysis of the food items.

4. **View the Results**: The app will display:
   - The total calories for each food item.
   - Whether the food is considered healthy.
   - A breakdown of carbohydrates, fats, fiber, and other nutrients.

---

## Code Structure

- `app.py`: Contains the main logic and Streamlit code for running the web app.
- `get_gemini_response()`: A function that sends an image and prompt to the Google Gemini Pro Vision API and returns a response.
- `input_image_setup()`: A helper function to process and prepare uploaded image data for the API.
- `.env`: Stores environment variables, including the Google API key.

---

## Example Input and Output

### Example Input
- An image of a meal containing a burger, fries, and a drink.

### Example Output
```
1. Burger - 400 calories
2. Fries - 300 calories
3. Soft Drink - 150 calories

Total Calories: 850
The meal is not considered healthy due to its high fat and sugar content.
Nutrient Breakdown:
- Carbohydrates: 50%
- Fats: 30%
- Fiber: 5%
- Sugar: 15%
```

---

## Limitations
- **Accuracy**: The accuracy of the calorie count and health analysis depends on the quality of the image and the capabilities of the Google Gemini Pro Vision API.
- **Food Variety**: Some less common food items might not be recognized properly by the API.

---

## Future Enhancements
- Add support for additional APIs for more precise food recognition.
- Implement user accounts to store daily food intake data.
- Integrate exercise tracking to provide a more holistic health management tool.

---

## License

This project is licensed under the MIT License.

---

## Contact

For questions or feedback, feel free to reach out to the project maintainer:

- **Email**: [hariharan.2023@vitstudent.ac.in](mailto:hariharan.2023@vitstudent.ac.in)
