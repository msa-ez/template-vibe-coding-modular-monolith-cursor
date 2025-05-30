### How To Use

1. Download the Project

Click the **'Download archive'** icon to download the project to your local repository as shown in the image.

<img width="794" alt="Image" src="https://github.com/user-attachments/assets/042bfe89-0305-4330-9709-aeaf12b12002" />

2. Rename the Rules Directory
In your IDE (Cursor, VSCode...), access the project and rename the clinerules folder to match Cline implementation requirements:

```
mv vibe-coding-rules .clinerules
```

3. Rename the Rules files.
You need to change the mdc extension files under .clinerules to md.
example: generation-rules.mdc > generation-rules.md
```
cd .clinerules
for file in *.mdc; do mv -- "$file" "${file%.mdc}.md"; done
```

4. Consolidation Metadata
Execute the command below to consolidate the Metadata from each domain service's PRD.txt into the modular-monolith-prompt.txt:
```
cat "modular-monolith-prompt.txt" {{#boundedContexts}}{{#aggregates}}{{nameCamelCase}}/PRD.txt {{/aggregates}}{{/boundedContexts}} > "modular-monolith-prompt.txt.new" && mv "modular-monolith-prompt.txt.new" "modular-monolith-prompt.txt"
```

5. Generate Code
Copy and paste the content from **modular-monolith-prompt.txt** into the Cline Prompt Input window to generate your code
