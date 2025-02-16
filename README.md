# File Sharing Platform with Django REST Framework (DRF)

![File Sharing Platform](https://via.placeholder.com/800x400?text=File+Sharing+Platform)

A simple and intuitive file-sharing platform built using **Django REST Framework (DRF)**. This project allows users to upload multiple files, generate shareable links, and download files securely. The frontend is designed with **Bootstrap** and **FilePond**, providing a modern and responsive user interface.

Uploaded files are stored locally on the server's filesystem in the `media/` directory. No database is used for storing file metadata; instead, file paths and unique identifiers are managed in memory or through lightweight configurations.

---

## Table of Contents

1. [Features](#features)
2. [Tech Stack](#tech-stack)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Screenshots](#screenshots)
6. [Contributing](#contributing)
7. [License](#license)

---

## Features

- **File Upload**: Users can upload multiple files at once using the FilePond library.
- **Shareable Links**: After uploading, a unique shareable link is generated for easy file sharing.
- **Responsive Design**: A mobile-friendly and visually appealing UI built with Bootstrap.
- **Clipboard Integration**: Copy the shareable link to the clipboard with a single click.
- **Secure Backend**: Built with Django REST Framework for robust and scalable APIs.
- **File Download**: Users can download files via the generated links.
- **Local File Storage**: Files are saved directly on the server's filesystem without relying on a database or cloud storage.

---

## Tech Stack

- **Backend**: Django, Django REST Framework (DRF)
- **Frontend**: HTML, CSS, Bootstrap, FilePond
- **File Storage**: Local filesystem (`media/` directory)
- **JavaScript**: jQuery for DOM manipulation and API calls
- **Other Tools**: FilePond for file uploads, Clipboard API for copying links

---

## Installation

### Prerequisites

- Python 3.8+
- Pip (Python package manager)
- Virtualenv (optional but recommended)

### Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/file-sharing-platform.git
   cd file-sharing-platform
   ```

2. **Set Up a Virtual Environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure Local File Storage**
   Uploaded files are saved in the `media/` directory by default. Ensure the following settings are configured in `settings.py`:

   ```python
   MEDIA_URL = '/media/'
   MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
   ```

5. **Start the Development Server**
   ```bash
   python manage.py runserver
   ```

6. **Access the Application**
   Open your browser and navigate to:
   ```
   http://127.0.0.1:8000/
   ```

---

## Usage

### Home Page
- **Upload Files**: Drag and drop files or click to browse and select multiple files.
- **Generate Link**: After uploading, a unique shareable link is generated automatically.
- **Copy Link**: Click the "Copy Shareable Link" button to copy the link to your clipboard.

### Download Page
- **Download Files**: Use the generated link to access the download page and retrieve the uploaded files.

---

## Local File Storage

Uploaded files are stored in the `media/` directory by default. The directory structure looks like this:


---

## Screenshots

### Home Page
![Home Page]()

The home page features a clean and intuitive interface for uploading files. Users can drag and drop files or use the browse button to select files. Once uploaded, a shareable link is generated.

### Download Page
![Download Page]()

The download page displays the uploaded files and provides a button to download them. The URL for this page is generated after file upload.

---

## Contributing

We welcome contributions! If you'd like to contribute to this project, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeatureName`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature/YourFeatureName`).
5. Open a pull request.

For major changes, please open an issue first to discuss what you’d like to change.

---

## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## Acknowledgments

- **Django REST Framework**: For building the backend API.
- **FilePond**: For handling file uploads with a beautiful UI.
- **Bootstrap**: For creating a responsive and modern frontend.
