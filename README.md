<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Random Coding Quote</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background-color: #f0f0f0;
      text-align: center;
      padding: 50px;
    }
    .quote-box {
      background: white;
      padding: 30px;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
      max-width: 600px;
      margin: auto;
    }
    .quote {
      font-size: 1.4rem;
      color: #333;
    }
    .author {
      margin-top: 10px;
      font-size: 1.1rem;
      color: #666;
    }
    button {
      margin-top: 20px;
      padding: 10px 20px;
      font-size: 1rem;
      cursor: pointer;
    }
  </style>
</head>
<body>

  <div class="quote-box">
    <div class="quote" id="quoteText">Loading quote...</div>
    <div class="author" id="quoteAuthor"></div>
    <button onclick="generateQuote()">🎲 New Quote</button>
  </div>

  <script>
    const quotes = [
      {
        text: "Talk is cheap. Show me the code.",
        author: "Linus Torvalds"
      },
      {
        text: "Programs must be written for people to read, and only incidentally for machines to execute.",
        author: "Harold Abelson"
      },
      {
        text: "First, solve the problem. Then, write the code.",
        author: "John Johnson"
      },
      {
        text: "Any fool can write code that a computer can understand. Good programmers write code that humans can understand.",
        author: "Martin Fowler"
      },
      {
        text: "Code never lies, comments sometimes do.",
        author: "Ron Jeffries"
      }
    ];

    function generateQuote() {
      const randomIndex = Math.floor(Math.random() * quotes.length);
      const quote = quotes[randomIndex];
      document.getElementById("quoteText").innerText = quote.text;
      document.getElementById("quoteAuthor").innerText = `— ${quote.author}`;
    }

    // Generate one on page load
    window.onload = generateQuote;
  </script>

</body>
</html>
