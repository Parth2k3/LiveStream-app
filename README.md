<h1>Overview</h1><br>
<p>This application allows users to stream video content using an RTSP URL and overlay customizable elements such as text and images. Users can create, read, update, and delete overlays, enhancing the streaming experience.</p><br>
<h1>Features</h1><br>
<p>Stream video using RTSP URLs.<br>
Create and manage text and image overlays.<br>
Save and load overlay configurations.<br></p>

<h1>API Documentation</h1><br>
<h3>Base URL</h3><br>
http://localhost:5000<br>

<h3>Endpoints</h3><br>
<h5>1. Create Overlay</h5>
<br><br>
POST /overlay<br>
Description: Create a new overlay configuration.<br>
Request Body:<br>
json<br>
<br>
{<br>
  "texts": [<br>
      {<br>
      "id": "unique_id",<br>
      "content": "Text content",<br>
      "position": {<br>
        "x": 100,<br>
        "y": 100<br>
      },<br>
      "fontSize": 18<br>
    }<br>
  ],<br>
  "logos": [<br>
    {<br>
      "id": "unique_id",<br>
      "src": "image_url",<br>
      "position": {<br>
        "x": 200,<br>
        "y": 200<br>
      },<br>
      "size": {<br>
        "width": 50,<br>
        "height": 50<br>
      }<br>
    }<br>
  ]<br>
}<br>

<h5>2. Get All Overlays</h5><br>
GET /overlay<br>
Description: Retrieve all saved overlays.<br>
Response:<br>
json<br>
<br>
[<br>
  {<br>
    "id": "unique_id",<br>
    "texts": [...],<br>
    "logos": [...]<br>
  }<br>
]<br>
<h5>3. Get Overlay by ID</h5>
GET /overlay/{id}<br>
Description: Retrieve a specific overlay configuration.<br>
Response:<br>
json<br>
<br>
{<br>
  "texts": [...],<br>
  "logos": [...]<br>
}<br>
<br>
<h5>6. Delete Overlay</h5><br>
DELETE /overlay/{id}<br>
Description: Delete a specific overlay configuration.<br>
User Documentation<br>
Setup<br>
Clone the Repository:<br>
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
