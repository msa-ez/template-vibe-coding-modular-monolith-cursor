### How To Use

1. Download the Project

Click the **'Download archive'** icon to download the project to your local repository as shown in the image.

<img width="794" alt="Image" src="https://github.com/user-attachments/assets/042bfe89-0305-4330-9709-aeaf12b12002" />

2. Rename the Rules Directory
In your IDE (Cursor, VSCode...), access the project and rename the cursorrules folder to match Cursor implementation requirements:

```
mkdir -p .cursor/rules
find vibe-coding-rules -type f -exec mv {} .cursor/rules/ \; && rm -rf vibe-coding-rules
```

3. Mode and Model Selection 
Press Ctrl + L to activate CursorIDE, then select Agent mode. After that, choose model as claude-3.7-sonnet or claude-3.7-sonnet-max.

<img width="373" alt="Image" src="https://github.com/user-attachments/assets/afe44a5e-458e-4afd-99dc-e44e92953bc1" />

4. Generate Code
Copy and paste the content from **PRD.txt** into the Cline Prompt Input window to generate your code
