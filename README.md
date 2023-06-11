# [twitterbio.io](https://www.twitterbio.io/)

This project generates Twitter bios for you using AI.

[![Twitter Bio Generator](./public/screenshot.png)](https://www.twitterbio.io)

## How it works

This project uses the [ChatGPT API](https://openai.com/api/) and [Vercel Edge functions](https://vercel.com/features/edge-functions) with streaming. It constructs a prompt based on the form and user input, sends it to the chatGPT API via a Vercel Edge function, then streams the response back to the application.

If you'd like to see how I built this, check out the [video](https://youtu.be/JcE-1xzQTE0) or [blog post](https://vercel.com/blog/gpt-3-app-next-js-vercel-edge-functions).

## Running Locally

After cloning the repo, go to [OpenAI](https://beta.openai.com/account/api-keys) to make an account and put your API key in a file called `.env`.

Then, run the application in the command line and it will be available at `http://localhost:3000`.

```bash
npm run dev
```

## One-Click Deploy

Deploy the example using [Vercel](https://vercel.com?utm_source=github&utm_medium=readme&utm_campaign=vercel-examples):

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/Nutlope/twitterbio&env=OPENAI_API_KEY&project-name=twitter-bio-generator&repo-name=twitterbio)


#Notes

I Replaced the "bio" variable with "text" to make it an input for any kind of text generation,and then updated the prompt and generated text labels to reflect the change in functionality.

modified the fetch request and response handling to work with the updated prompt and generated text.

Replaced the "generatedBios" state with "generatedText" to store and display the generated text.

For the database, I would use a NoSQL database because 

Change the table structure: Modify the structure of the database table to accommodate the academic context. Instead of storing Twitter bio-related information, create new tables to store academic-related information such as text samples, topics, authors, timestamps, etc. Connect the tables with foreign keys and join them based on topic, author, e.t.c

I deally I would store some of the data in a NoSQL db like MongoDB