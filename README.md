# Healthcare Dashboard Project

This project consists of a **React** frontend and a **Flask** backend, where users can submit their name, age, and upload a file (e.g., medical reports or documents). The file is processed and saved on the server.

## **Technologies Used**
- **Frontend**: React.js
- **Backend**: Flask (Python)
- **File Upload**: FormData (React) and Flask `request.files` for handling uploads
- **CORS**: Enabled for cross-origin requests between React (port 3000) and Flask (port 5000)

## **Features**
- Input fields for Name and Age
- File upload functionality
- File is saved to the server upon submission
- Simple UI for healthcare-related data submission

## **Project Structure**
```
/healthcare-dashboard
    /flask
        app.py               # Flask backend to handle file uploads
    /react
        /src
            App.js           # React frontend with form and file upload
        package.json         # React dependencies and scripts
    /uploads                  # Folder where uploaded files are saved (create this manually)
```

## **Setup Instructions**

### **Step 1: Backend Setup (Flask)**

1. Navigate to the `flask` directory in your terminal.
   
2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   ```

3. Install the required Python dependencies:
   ```bash
   pip install flask flask-cors
   ```

4. Create a folder named `uploads` to store uploaded files:
   ```bash
   mkdir uploads
   ```

5. Start the Flask server:
   ```bash
   python app.py
   ```

   The Flask server will run at `http://127.0.0.1:5000`.

### **Step 2: Frontend Setup (React)**

1. Navigate to the `react` directory in your terminal.
   
2. Install the required dependencies:
   ```bash
   npm install
   ```

3. Start the React development server:
   ```bash
   npm start
   ```

   The React app will run at `http://localhost:3000`.

---

## **How to Use the Dashboard**

1. Open the React app in your browser (`http://localhost:3000`).
2. Enter your **Name** and **Age** in the input fields.
3. Choose a **File** (such as a medical document) to upload.
4. Click the **Submit** button to send the data to the Flask server.
5. You will see a success message if the upload is successful or an error message if there was an issue.

---

## **Endpoints**

### **POST /api/upload**
- **Description**: Accepts the file, name, and age from the frontend.
- **Expected Data**:
  - `name` (string): The user's name
  - `age` (integer): The user's age
  - `file`: The file to be uploaded (e.g., a medical report)

