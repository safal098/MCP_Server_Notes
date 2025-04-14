# AI Sticky Notes

A simple yet powerful sticky notes application with email notification capabilities.

## Features

- **Add Notes**: Quickly add notes to your collection
- **Read Notes**: View all your saved notes
- **Delete Notes**: Remove unwanted notes by their position
- **Get Latest Note**: Retrieve the most recent note
- **Email Notifications**: Receive email alerts when new notes are added
- **Note Summarization**: Generate summaries of your notes using AI

## Installation

1. Clone this repository:
   ```
   git clone <repository-url>
   cd <repository-directory>
   ```

2. Create and activate a virtual environment:
   ```
   python -m venv venv
   # On Windows
   venv\Scripts\activate
   # On macOS/Linux
   source venv/bin/activate
   ```

3. Install the required dependencies:
   ```
   pip install -r requirements.txt
   ```

## Gmail API Setup

To enable email notifications, you need to set up the Gmail API:

1. Go to the [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project or select an existing one
3. Enable the Gmail API for your project
4. Go to "Credentials" and create an OAuth 2.0 Client ID
5. Choose "Desktop application" as the application type
6. Download the credentials and save them as `credentials.json` in the project directory

The first time you run the application, it will open a browser window asking you to authorize the application. After authorization, it will create a `token.pickle` file for future use.

## Usage

Run the application:
```
python main.py
```

### Available Commands

- **Add a note**: `add_note("Your note text")`
- **Read all notes**: `read_notes()`
- **Delete a note**: `delete_note(index)` (where index is the position of the note, starting from 1)
- **Get latest note**: Access the resource at `notes://latest`
- **Generate note summary**: Use the `note_summary_prompt()` function

## File Structure

- `main.py`: The main application file
- `notes.txt`: Storage file for all notes
- `credentials.json`: Gmail API credentials (not included in repository)
- `token.pickle`: Authentication token for Gmail API (generated on first run)
- `requirements.txt`: List of Python dependencies

## License

[MIT License](LICENSE)

## Author

Safal Sharma
