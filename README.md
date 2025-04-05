<!DOCTYPE html>
<html>
<head>
    <title>Code Copy Example</title>
    <style>
        /* Container styling */
        .code-container {
            position: relative;
            margin: 20px 0;
            background: #f5f5f5;
            border-radius: 4px;
            border: 1px solid #ddd;
        }
        
        /* Code block styling */
        pre {
            padding: 15px;
            margin: 0;
            overflow-x: auto;
            white-space: pre-wrap;
        }
        
        /* Copy button styling */
        .copy-button {
            position: absolute;
            top: 5px;
            right: 5px;
            padding: 5px 10px;
            background: #f1f1f1;
            border: 1px solid #ccc;
            border-radius: 4px;
            cursor: pointer;
            font-size: 12px;
        }
        
        .copy-button:hover {
            background: #e1e1e1;
        }
    </style>
</head>
<body>
    <h1>Copyable Code Example</h1>
    
    <div class="code-container">
        <pre><code id="codeBlock1">function example() {
  console.log("Hello world");
  return true;
}</code></pre>
        <button class="copy-button" onclick="copyCode('codeBlock1')">Copy</button>
    </div>

    <script>
        function copyCode(elementId) {
            // Get the text content
            const codeElement = document.getElementById(elementId);
            const textToCopy = codeElement.textContent;
            
            // Use the Clipboard API
            navigator.clipboard.writeText(textToCopy)
                .then(() => {
                    // Provide visual feedback
                    const button = event.target;
                    const originalText = button.textContent;
                    button.textContent = 'Copied!';
                    
                    // Reset button text after 2 seconds
                    setTimeout(() => {
                        button.textContent = originalText;
                    }, 2000);
                })
                .catch(err => {
                    console.error('Failed to copy text: ', err);
                    alert('Failed to copy code. Please try again or copy manually.');
                });
        }
    </script>
</body>
</html>
