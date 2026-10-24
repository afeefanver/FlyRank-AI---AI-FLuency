Voice card: Direct, plain, honest, specific, no buzzwords. Use my words and my numbers. Cut anything I couldn't say out loud.

Piece 1: Vector, plain-English answers from your own business data

The problem. Most small business owners in Kerala keep their sales and stock in spreadsheets and have no analyst. They know the answers are in there, but getting them means asking someone else or doing it by hand. Asking a language model to read the numbers directly isn't the fix, because it makes arithmetic mistakes, and a wrong number is worse than no number.

What I did and what I decided. At MIS Data Automate I built Vector so an owner can type a question in plain English and get an answer and a chart back. The decisions that mattered:

Numbers come from code, not the model. pandas does the calculation, and the language model only explains the result. That is how I stopped it inventing figures.

Two models for two jobs. qwen2.5-coder:7b writes the structured chart output, and phi3 handles the faster answers on ordinary CPUs.

Run it where the data lives. Vector could run on the owner's own machine or in the cloud, so nobody has to ship their sales data somewhere they don't trust.

Price it so a small shop says yes. I moved from prepaid credits to a monthly subscription starting at 999 rupees a month. With prepaid credits an owner counts every question before asking it. A flat monthly price lets them ask freely, and 999 is a price a small shop can say yes to.

After launch I found it still got things wrong, so I rebuilt it around 155 structured test cases and kept fixing until none failed.

What came of it. The version I built passed all 155 test cases with zero errors. If your business has data like this, book a 20-minute call and I'll show you what your own questions would return.

Piece 2: Running a one-month AI internship

The problem. Three interns were joining a live product with little experience of language models. Dropping them straight into the codebase risked breaking things and teaching them nothing.

What I did and what I decided. I put learning before access. Each intern started with small, isolated tasks and LLM reading, and only then touched the real code. They worked on three tracks: testing the language model, testing the product, and a capstone AI Note Generator.

What came of it. The capstone became a working Education AI module: an AI Note Generator and an AI Tutor Chat on a RAG pipeline (Ollama, ChromaDB, FastAPI, React), shown in a structured demo on the final day. All three interns got internship certificates. Weeks later they organized and ran a two-day hands-on workshop, From Prompt to Product, at ICET, which is the clearest thing they could do at the end that they couldn't at the start.

Piece 3: How my page puts my name in the middle and keeps my colors in one place

My whole site right now is one file, index.html. The name sits in the exact center of the screen because of three lines of CSS. I made the page and its body as tall as the screen (height: 100%), then told the body to act like a grid (display: grid) and to put its content in the middle (place-items: center). Without the height line, the body would only be as tall as my text, so "center" would mean the top of the screen.

For colors, I wrote my palette once at the top as named variables, like --main for my teal. Wherever I want teal, I write var(--main). If I change the color later, I edit one line instead of searching the whole file.

The font isn't on my computer. A link in the page asks Google Fonts to send Space Grotesk, and if that fails the browser falls back to a plain sans-serif.
