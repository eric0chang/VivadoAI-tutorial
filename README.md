style="border:3px solid #FFFFFF;border-radius:8px;box-shadow:0 0 10px rgba(255,255,255,0.4);"

# VivadoAI-tutorial
This document will guide user how to link remote server and setup LLM and Vivado AI MCP. And experience AI-driven FPGA development.



## Connect Remote Server through SSH
- connect server with username, password and IP address
  - modify username/password with requirement, `amd-user1@210.61.209.139:45091`

<img width="3200" height="958" alt="image" src="https://github.com/user-attachments/assets/d1cba477-5255-4e77-96e1-5bf7eaffc1bc" />

- Open Folder as wrokspace and input password again

<img width="2284" height="1088" alt="image" src="https://github.com/user-attachments/assets/7bb68641-c70f-4a12-b606-5925c03487e7" />

<img width="3200" height="592" alt="image" src="https://github.com/user-attachments/assets/a33d123a-ec67-4a04-91ae-aa58a1f0bf34" />



## Setup Local LLM
- Select **Manage Models...** in CHAT box

<img width="3200" height="1324" alt="image" src="https://github.com/user-attachments/assets/fa7595bb-366a-4392-8ed0-f97c0d8cb0e1" />

- Press **Add Models** and Select **Custom Endpoint**

<img width="2530" height="668" alt="image" src="https://github.com/user-attachments/assets/883c9545-d2a3-45ba-9b7a-f859ff254df1" />

- Keep **Group Namd** and **API Key** as default, and select **Chat Completions Chat Completions API**


<img width="303" height="57" alt="image" src="https://github.com/user-attachments/assets/522278a9-131e-44d6-b868-b1b2cd247052" />

<img width="1220" height="224" alt="image" src="https://github.com/user-attachments/assets/26bfe271-c28b-4044-8a40-1d6e449cf4c3" />

<img width="1212" height="294" alt="image" src="https://github.com/user-attachments/assets/e38b063d-9d98-4f19-95ca-2da5169377d1" />

- Edit .json file and save
  ```
    [
        {
            "name": "Local vLLM",
            "vendor": "customendpoint",
            "apiKey": "dummy",
            "apiType": "chat-completions",
            "models": [
                {
                    "id": "openai/gpt-oss-120b",
                    "name": "GPT-OSS 120B (vLLM)",
                    "url": "http://192.168.10.105:45827/v1/",
                    "toolCalling": true,
                    "vision": false,
                    "maxInputTokens": 120000,
                    "maxOutputTokens": 8000,
                    "thinking": true
                }
            ]
        }
    ]
  ```

<img width="2576" height="950" alt="image" src="https://github.com/user-attachments/assets/488293b8-f419-47b8-964a-d81fda5016da" />





<img width="3200" height="1546" alt="image" src="https://github.com/user-attachments/assets/83300987-858f-4735-9eb8-6b6941766765" />

<img width="3200" height="1542" alt="image" src="https://github.com/user-attachments/assets/b5a1c7c6-66c2-4ae4-b73d-414eb9e590e4" />


<img width="3207" height="956" alt="image" src="https://github.com/user-attachments/assets/e1fd8c51-38a1-4f6d-a758-77e4ada35d5a" />

<img width="3200" height="850" alt="image" src="https://github.com/user-attachments/assets/57fd1fa2-befa-4433-a11c-08a4d395849f" />

<img width="724" height="948" alt="image" src="https://github.com/user-attachments/assets/292f0d32-55e3-4633-8fe7-1d6e741b277e" />









