NodeJS:
import Portkey from 'portkey-ai';

const portkey = new Portkey({
  apiKey: "ENTER_YOUR_KEY"
});

async function main() {
  const response = await portkey.chat.completions.create({
    messages: [
      { role: "system", content: "You are a helpful assistant" },
      { role: "user", content: "What is Portkey" }
    ],
    model: "@csuite-zai/chat",
    MAX_TOKENS: 512
  });

  console.log(response.choices[0].message.content);
}

main();

Python:
from portkey_ai import Portkey

portkey = Portkey(
  api_key = "ENTER_YOUR_KEY"
)

response = portkey.chat.completions.create(
    model = "@csuite-zai/chat",
    messages = [
      {"role": "system", "content": "You are a helpful assistant."},
      {"role": "user", "content": "What is Portkey"}
    ],
    MAX_TOKENS = 512
)

print(response.choices[0].message.content)

OpenAI Python SDK:
from openai import OpenAI
from portkey_ai import PORTKEY_GATEWAY_URL

portkey = OpenAI(
  base_url = PORTKEY_GATEWAY_URL,
  api_key = "ENTER_YOUR_KEY"
)

response = portkey.chat.completions.create(
    model = "@csuite-zai/chat",
    messages = [
      {"role": "system", "content": "You are a helpful assistant."},
      {"role": "user", "content": "What is Portkey"}
    ],
    MAX_TOKENS = 512
)

print(response.choices[0].message.content)

OPENAI Nodejs SDK:
import OpenAI from 'openai';
import { PORTKEY_GATEWAY_URL } from 'portkey-ai';

const portkey = new OpenAI({
  baseURL: PORTKEY_GATEWAY_URL,
  apiKey: "ENTER_YOUR_KEY"
});

async function main() {
  const response = await portkey.chat.completions.create({
    messages: [
      {"role": "system", "content": "You are a helpful assistant."},
      { role: “user”, content: “What is Portkey” }
    ],
    model: '@csuite-zai/chat',
    MAX_TOKENS: 512
  });

  console.log(response.choices[0].message.content);
}

main();

CURL:
curl https://api.portkey.ai/v1/chat/completions   -H "Content-Type: application/json"   -H "x-portkey-api-key: ENTER_YOUR_KEY"   -d '{
    "model": "@csuite-zai/chat",
    "messages": [
      {"role": "system", "content": "You are a helpful assistant."},
      {"role": "user", "content": "What is Portkey"}
    ],
    "MAX_TOKENS": 512
  }'

  
