# OpenWise
Project OpenWise
<h1>OpenWise test</h1>
<p>Blah blah blah</p>
<p>Blah blah blah</p>
<p>Blah blah blah</p>
<p>See Daniel?</p>

<div class="code-container">
  <pre id="codeBlock1"><code>function example() { 
  console.log("Hello world");
}</code></pre>
  <button class="copy-button" data-target="codeBlock1">Copy</button>
</div>

<script>
document.querySelectorAll('.copy-button').forEach(button => {
  button.addEventListener('click', () => {
    const targetId = button.getAttribute('data-target');
    const textToCopy = document.getElementById(targetId).textContent;
    
    navigator.clipboard.writeText(textToCopy)
      .then(() => {
        // Visual feedback
        button.textContent = 'Copied!';
        setTimeout(() => {
          button.textContent = 'Copy';
        }, 2000);
      })
      .catch(err => {
        console.error('Failed to copy: ', err);
      });
  });
});
</script>
