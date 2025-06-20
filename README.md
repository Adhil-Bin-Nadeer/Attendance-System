# Face Recognition Attendance System

A Python-based attendance system that uses facial recognition and smile detection to automatically record attendance data to Google Sheets.

## 🌟 Features

- **Face Detection**: Automatically detects faces using OpenCV
- **Smile Recognition**: Requires users to smile for attendance confirmation
- **Google Sheets Integration**: Automatically saves attendance data to Google Sheets
- **Interactive UI**: User-friendly interface with visual feedback
- **Voice Prompts**: Audio instructions to guide users
- **Duplicate Prevention**: Prevents duplicate entries for the same person
- **Real-time Processing**: Live webcam feed with instant face detection

## 🚀 How It Works

1. **Start Screen**: Click the start button to begin
2. **Smile Detection**: Look into the camera and smile
3. **Name Entry**: Enter your name when prompted
4. **Attendance Recording**: Your attendance is automatically saved to Google Sheets
5. **Confirmation**: View your attendance confirmation with a unique token

## 📋 Requirements

- Python 3.7+
- Webcam
- Google Sheets API credentials
- Required Python packages (see Installation)

## 🛠️ Installation

1. **Clone the repository**:
   ```bash
   git clone <your-repository-url>
   cd Attendance-System
   ```

2. **Install required packages**:
   ```bash
   pip install opencv-python
   pip install google-api-python-client
   pip install google-auth
   pip install pyttsx3
   pip install tkinter
   ```

3. **Set up Google Sheets API**:
   - Go to [Google Cloud Console](https://console.cloud.google.com/)
   - Create a new project or select an existing one
   - Enable the Google Sheets API
   - Create service account credentials
   - Download the JSON key file
   - Place the JSON file in the project directory

4. **Configure the application**:
   - Open `config.py`
   - Update `SPREADSHEET_ID` with your Google Sheets ID
   - Update `CREDENTIALS_FILE` with your JSON key file name

5. **Prepare background images**:
   - Place your background images in the `Background/` folder:
     - `Desktop Inital.png` - Start screen background
     - `Desktop input.png` - Smile detection background
     - `Desktop final.png` - Final confirmation background
     - `new.png` - Face recognition background

## 🎯 Usage

1. **Run the application**:
   ```bash
   python main.py
   ```

2. **Follow the on-screen instructions**:
   - Click "Start" to begin
   - Look into the camera and smile
   - Enter your name when prompted
   - Wait for confirmation

3. **Press 'q' to quit** the application

## 📁 Project Structure

```
Attendance-System/
├── main.py              # Main application file
├── config.py            # Configuration settings
├── vision.py            # Face and smile detection
├── ui_manager.py        # User interface management
├── sheets_manager.py    # Google Sheets integration
├── utils.py             # Utility functions
├── Background/          # Background images
├── Recognition_models/  # Face detection models
└── README.md           # This file
```

## ⚙️ Configuration

### Google Sheets Setup
1. Create a Google Sheet with columns: Name, Token
2. Copy the spreadsheet ID from the URL
3. Update `config.py` with your spreadsheet ID

### Camera Settings
- The system uses the default camera (index 0)
- Camera resolution is automatically configured
- ROI (Region of Interest) can be adjusted in `config.py`

## 🔧 Troubleshooting

### Common Issues

1. **Camera not working**:
   - Ensure your webcam is connected and not used by other applications
   - Try changing the camera index in `main.py`

2. **Google Sheets not updating**:
   - Check your internet connection
   - Verify your API credentials
   - Ensure the spreadsheet is shared with the service account email

3. **Face not detected**:
   - Ensure good lighting
   - Position your face clearly in the camera view
   - Check if the cascade files are properly loaded

4. **Import errors**:
   - Install all required packages
   - Check Python version compatibility

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Dependencies

- **OpenCV**: Computer vision and image processing
- **Google API Client**: Google Sheets integration
- **pyttsx3**: Text-to-speech functionality
- **tkinter**: GUI components

---

**Note**: Make sure to keep your Google Sheets API credentials secure and never commit them to public repositories.
