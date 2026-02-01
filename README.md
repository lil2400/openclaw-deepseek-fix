# 🦞 **DeepSeek on OpenClaw: The Working Way**

I wasted an hour of my life debugging OpenClaw's config so you don't have to. If you are seeing `baseUrl: undefined` or your bot keeps crashing because it defaults to Anthropic, this is the fix.

## 🚀 **The 1-Minute Fix**

### **Step 1: Define the Provider**
OpenClaw 2026 requires the `baseUrl` and the `models` array to be defined manually. Run this command (replace `YOUR_KEY` with your actual DeepSeek API key):

```bash
openclaw config set models.providers.deepseek '{
  "baseUrl": "[https://api.deepseek.com/v1](https://api.deepseek.com/v1)",
  "apiKey": "YOUR_KEY",
  "api": "openai-completions",
  "models": [{"id": "deepseek-chat"}]
}'
