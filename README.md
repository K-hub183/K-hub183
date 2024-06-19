- 👋 Hi, I’m @K-hub183
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
K-hub183/K-hub183 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import requests

def generate_request(query, max_tokens=500, temperature=0.7, system_prompt="Be Helpful and Friendly. Keep your response straightfoward, short and concise"):
    url = "https://devsdocode-openrouter.hf.space/generate"
    params = {
        "query": query,
        "max_tokens": max_tokens,
        "temperature": temperature,
        "system_prompt": system_prompt
    }
    response = requests.get(url, params=params)
    return response.json()

if __name__ == "__main__":
    # Example usage:
    query = "Write 20 lines about India each in different languages"
    response = generate_request(query, max_tokens=500, temperature=0.7)
    print(response[0]['response'])
    
