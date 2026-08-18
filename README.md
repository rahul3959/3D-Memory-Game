# Markdown content for the README
README_CONTENT = """# 🃏 3D Memory Matching Game

A lightweight, interactive 3D memory card game built using **Python (Flask)**, **Three.js**, and **Bootstrap 5**. The project features a responsive WebGL rendering canvas, custom procedural textures, smooth 3D card-flip animations, raycasting interaction, and real-time score tracking.

---

## 🚀 Features

- **3D Graphics & Animations**: Powered by Three.js with smooth rotational animations (`lerp`) and real-time lighting/shadows.
- **Procedural Textures**: Generates card faces and backs dynamically on HTML5 Canvas without relying on external image assets.
- **Interactive UI**: Built with Bootstrap 5 overlay components showing move counters, current match status, and game controls.
- **Raycasting Interaction**: Uses 3D object picking (`THREE.Raycaster`) to handle user clicks directly on 3D meshes.
- **Clean Flask Backend**: Simple Python web server providing render endpoints for client-side evaluation.

---

## 🛠️ Tech Stack

- **Backend**: Python 3, Flask
- **Frontend Framework**: Bootstrap 5 (CSS/JS via CDN)
- **3D Engine**: Three.js (WebGL via CDN)
- **Languages**: HTML5, CSS3, JavaScript (ES6+)

---

## 📂 Project Structure

```text
memory_game/
├── app.py              # Main Flask server script
├── templates/
│   └── index.html      # Game canvas, Bootstrap layout, and embedded JS game engine
└── README.md           # Project documentation
⚙️ Installation & Setup
Prerequisites
Make sure you have Python 3.8+ installed on your system.

1. Clone the Repository
Bash
git clone [https://github.com/your-username/3d-memory-game.git](https://github.com/your-username/3d-memory-game.git)
cd 3d-memory-game
2. Set Up a Virtual Environment (Optional but Recommended)
Bash
# On Linux/macOS
python3 -m venv venv
source venv/bin/activate

# On Windows
python -m venv venv
venv\\Scripts\\activate
3. Install Dependencies
Install Flask using pip:

Bash
pip install flask
🎮 Running the Game
Start the Flask application:

Bash
python app.py
Open your web browser and navigate to:

Plaintext
[http://127.0.0.1:5000](http://127.0.0.1:5000)
🎯 How to Play
Click on any card in the 3D grid to flip it and reveal its color.

Select a second card to find a match.

Match: If both cards match in color, they stay face-up.

Mismatch: If colors differ, the cards automatically flip back down after 1 second.

Complete all 6 pairs in as few moves as possible.

Press Restart Game at any time to re-shuffle the cards and reset your score.

📜 License
This project is open-source and available under the MIT License.
"""

def generate_pdf():
pdf = MarkdownPdf(toc=False)
pdf.add_section(Section(README_CONTENT))
output_filename = "README.pdf"
pdf.save(output_filename)
print(f"Success! '{output_filename}' has been generated in {os.getcwd()}")

if name == "main":
generate_pdf()


---

### How to Run

Execute the script directly from your terminal:

```bash
python convert.py
It will automatically compile the embedded markdown and generate README.pdf in the same directory.
