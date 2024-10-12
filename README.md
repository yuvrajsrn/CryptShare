# CryptShare

## Abstract
CryptShare is a secure cloud storage application compatible with popular platforms like Dropbox, Box, Google Drive, and Office 365. It encrypts uploaded files, allowing decryption only for members of a designated "Secure Cloud Storage Group." Developed using Python, open-source cryptographic libraries, and the Google Drive API, it features user authentication, user management, encryption/decryption, and a graphical user interface (GUI). Future enhancements may include hybrid key management and improved GUI security.

## Workflow
The application creates a private cloud space for securely uploading and downloading files. Users can be added or removed from this space, with files encrypted before uploading. Authentication is required to access the private space, and authorization (key) is needed to download files.

## Implementation

### User Management
The application checks for registered users and prompts for admin account creation if none exist. Admin privileges allow user management and key generation, with secure credential storage using pickling.

### Google Drive API Integration
It interfaces with the Google Drive API for file operations. Functions like `uploadFile()` and `downloadFile()` handle encrypted files, while `Encrypt()` and `Decrypt()` ensure secure data handling.

### Menu Generation
The admin menu provides options for user management and key generation, while standard users access file management features.

### Encryption/Decryption
The application uses the Fernet encryption scheme from the cryptography library, with secure key generation and retrieval.

### Authentication
Google Drive authentication adheres to the guidelines in the Google Drive API QuickStart guide for secure cloud access.

### Graphical User Interface (GUI)
Built with the Eel library, the application integrates Python backend functions with an HTML, CSS, and JavaScript frontend for an intuitive user experience.

## How to Run This Project
1. Create a Google Drive API credential named `client_secret.json` and save it in the `src` directory.
2. Run `main.exe` or execute `main.py`.

## Future Enhancements
- Hybrid key management for improved security.
- Enhanced GUI features for better user experience.
