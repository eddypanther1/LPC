**Local Persistent Clipboards:  Product Requirements Document (PRD)**

#### **Project Title:**

Standalone Windows Clipboard Manager GUI App

#### **Overview:**

Develop a standalone, stylistically modern yet minimalist clipboard manager application for Windows (Windows 10/11), utilizing a GUI library in vogue with modern developer tools (e.g., used in ChatGPT, GitHub Copilot). The application includes multi-clipboard support, persistent storage, and edit/run modes for flexible usage.

---

### **Target Platform:**

* Windows 10, 11 (64-bit)

---

### **GUI Design Requirements:**

* Use a modern, minimal GUI framework (e.g., Tauri, Electron, or native Windows libraries with CSS-like styling).

* UI elements should follow aesthetic trends of tools like ChatGPT or Copilot:

  * Rounded corners

  * Minimal shadows

  * Icon-based buttons for saving, settings, and mode toggling

  * Smooth transitions between modes

---

### **Core Features:**

#### **1\. Clipboard Management**

* Multi-clipboard support

* Persist clipboard contents between sessions

* Save either individual clipboard entries or all at once via save icon

* Support for storing multiple data types (text, images, possibly files)

#### **2\. Two Modes of Operation:**

##### **Run Mode (Default)**

* Shown on app start unless first-time run with no data → then start in Edit Mode

* Displays all stored clipboard entries in their proper format

  * Text entries in editable fields

  * Icons/buttons for one-click copy of specific data types

* Each entry has a “copy” icon that triggers a small non-intrusive “Copied” notification

* “Toggle Edit Mode” button (bottom-left corner)

##### **Edit Mode**

* Displays a list of clipboard entries in editable fields

* Special rows:

  * `add row` for inserting new clipboard entries

  * `csv_buttons` row (used for spawning  one click-button  for cvs separated special-characters or short-abbreviation)

* Editable fields allow:

  * Typing directly

  * Copy/paste

  * Individual or global save actions

* “Toggle Run Mode” button (bottom-left corner)

---

### **Settings (accessed via gear icon):**

* Adjust transparency of the app window

* Pin window to stay on top

---

### **Storage Requirements:**

* Persist clipboard entries locally across sessions

* Support for saving both text and multimedia (image, rich text, etc.)

##### **Open Issue:**

* Define how multimedia content (images, file blobs, etc.) will be stored:

  * Options: file-based storage, Base64 in JSON, etc.

If possible, stored standard allowable non-text multimedia as a file referenced in json

Example JSON: 

Demonstrating: 

Order: order to be displayed (must be unique)

Type:  “regular”, “csv\_button”, “multimedia”

{

  "order": "1",

  "type": "regular",

  "content": "including: frequently, repeatedly, often used phrases"

},

{

  "order": "2",

  "type": "csv\_button",

  "content": "😀,✅,⭕,ⓒ,☒,(火),(水)"

},

{

  "order": "3",

  "type": "multimedia",

  "content": "yyyymmddhhss.png"

}

---

### **Icons and Interactions:**

* Save icon: to save individual clipboard entry (in edit mode)

* Settings icon: opens transparency and pin settings

* Mode toggle icon (bottom-left): switches between Run/Edit mode

* Copy icon: copies entry to clipboard (in run mode)

---

### **Assets to be Referenced:**

* `edit_mode.png`

* `run_mode.png`

These mockups define UI layout, special row types, button placements.

But make it look better than the mockups with stylish minimalist intuitive responsive icon

---

### **Open Issues / To Be Discussed:**

1. **Choice of GUI Library:** Should we use Tauri, Electron, Qt, or a native Windows framework? \> Stylish, easy to understand, and easy to modify

2. **Storage Format for Clipboard Entries:**

   * JSON, SQLite, custom file format? \> JSON

   * How to persist multimedia (image or non-text) content? \> See JSON example

3. **Clipboard Types Supported:** Text and image, but should file references, formatted HTML or RTF be supported? \> Plain text and image for now

4. **CSV Import/Export Functionality:**

   * Scope and format for `csv_buttons` row \> see mockup in edit\_mode.png, each value for example { ⭕,ⓒ,☒,(火)} will spawn its only one-click pressible icon to copy the value into clipboard, so when user ctrl-v in a note takiang app that value (symbok or short phrase) would be pasted in

5. **App Packaging and Distribution:**

   * Should the app be installable via MSI or portable executable? \> portable executable

6. **Localization/Internationalization:**

   * Should we prepare for double-byte language support (JP/CH)? \> Must support double-byte (esp. JP)

7. **System Tray Icon or Background Service:**

   * Does the app need to monitor clipboard in background? \> for the last row, yes, it will refresh when copied

---

