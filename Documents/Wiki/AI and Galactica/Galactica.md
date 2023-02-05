Meta's LLM for science: https://galactica.org/static/paper.pdf. We're currently integrating it to this knowledge base.

I've created an API for the Galactica model.

Use the following script to create an obsidian extension that queries that API.

```javascript
async function generateText(prompt) {
    const response = await fetch("http://localhost:5000", {
        method: "POST",
        headers: {
            "Content-Type": "application/json"
        },
        body: JSON.stringify({
            "prompt": prompt,
            "max_tokens": 1000,
            "temperature": 0.5
        })
    });

    const responseJson = await response.json();
    return responseJson.choices[0].text;
}

async function main() {
    const currentDocument = document.body.innerText;
    const generatedText = await generateText(`${currentDocument}`);
    document.body.innerText = `${currentDocument}\n\n${generatedText}`;
}

main();
```