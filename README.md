# GM File Management System

This project provides a robust file management system for GameMaker Studio. It allows you to handle file creation, reading, and saving with ease.

## Getting Started
To initialize the file management system, you **must call `init_files()` at the start of your game**. This ensures that necessary file directories and structures are properly set up.

### Setup Steps
1. Import the `File_manager` folder into your GameMaker project.
2. In your game start event, include the following call:
   ```gml
   init_files();
   ```
   This function sets up required directories and checks for existing save data.

---

## Function Descriptions
Below is an overview of the key functions included in this project:

### `init_files()`
- **Purpose**: Initializes the file management system.
- **Details**: Creates necessary folders and checks for required files. This must be called at game start.

### `save_data(filename, data)`
- **Purpose**: Saves data to a specified file.
- **Parameters**:
  - `filename` (string): The name of the file to save.
  - `data` (string/array): The data to save in the file.
- **Example**:
   ```gml
   file_save("save1.sav", "player_position: 100, 200");
   ```

### `load_data(filename)`
- **Purpose**: Loads data from a specified file.
- **Parameters**:
  - `filename` (string): The name of the file to load.
- **Returns**: Data from the file or `null` if the file does not exist.
- **Example**:
   ```gml
   var data = file_load("save1.sav");
   ```

---

## Notes
- Ensure `init_files()` is called **once** at game start.
- Use descriptive file names to avoid conflicts.
- Always check if a file exists before attempting to load it.

---

## Project Structure
- `File_manager` Folder: Contains all scripts and objects for file management.
- `scripts/Filemanage/Filemanage.gml`: Core script handling all file operations.
- `objects/Ofilemanager`: Manages file events and logic.

---

## Future Improvements
- Add support for file encryption.
- Implement error handling for read/write operations.

---

Thank you for using the GM File Management System. Happy coding!
