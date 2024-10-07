<h1>Overview</h1><br>
<p>This application allows users to stream video content using an RTSP URL and overlay customizable elements such as text and images. Users can create, read, update, and delete overlays, enhancing the streaming experience.</p><br>
<h1>Features</h1><br>
<p>Stream video using RTSP URLs.<br>
Create and manage text and image overlays.<br>
Save and load overlay configurations.<br></p>

<h1>API Documentation</h1><br>
<h3>Base URL</h3><br>
http://localhost:5000

Endpoints
1. Create Overlay
POST /overlay
Description: Create a new overlay configuration.
Request Body:
json
Copy code
{
  "texts": [
      {
      "id": "unique_id",
      "content": "Text content",
      "position": {
        "x": 100,
        "y": 100
      },
      "fontSize": 18
    }
  ],
  "logos": [
    {
      "id": "unique_id",
      "src": "image_url",
      "position": {
        "x": 200,
        "y": 200
      },
      "size": {
        "width": 50,
        "height": 50
      }
    }
  ]
}
3. Get All Overlays
GET /overlay
Description: Retrieve all saved overlays.
Response:
json
Copy code
[
  {
    "id": "unique_id",
    "texts": [...],
    "logos": [...]
  }
]
4. Get Overlay by ID
GET /overlay/{id}
Description: Retrieve a specific overlay configuration.
Response:
json
Copy code
{
  "texts": [...],
  "logos": [...]
}
5. Update Overlay
PUT /overlay/{id}
Description: Update a specific overlay configuration.
Request Body: Same as the create overlay body.
6. Delete Overlay
DELETE /overlay/{id}
Description: Delete a specific overlay configuration.
User Documentation
Setup
Clone the Repository:
bash
Copy code
git clone https://github.com/yourusername/your-repo-name.git
Navigate to the Project Directory:
bash
Copy code
cd your-repo-name
Install Dependencies: For the backend (Flask):
bash
Copy code
cd backend
pip install -r requirements.txt
For the frontend (React):
bash
Copy code
cd frontend
npm install
Start the Backend:
bash
Copy code
cd backend
python app.py
Start the Frontend:
bash
Copy code
cd frontend
npm start
Using the Application
Open your browser and go to http://localhost:3000.
Input the RTSP URL for the video stream in the specified field.
Click "Start Stream" to begin the video playback.
Managing Overlays
Add Text: Click on "Add Text" and input your text. You can drag it to reposition.
Add Logo: Upload an image file to add a logo overlay.
Save Overlay: Click on "Save Overlay" to save your current overlays.
Load Overlay: Select a saved overlay from the dropdown to apply it.
