# Gurrom Flow SMS API 🚀

Send SMS in seconds via a simple, reliable REST API.

✔ Fast integration  
✔ Built for transactional messaging  
✔ Scalable (350k+ SMS/month infrastructure)  
✔ South Africa-ready 🇿🇦  

---

## ⚡ Send Your First SMS in 60 Seconds

### Endpoint

POST https://api.flow.gurrom.co.za/api/messageapi/sendmessage

---

### 🔐 Authentication

Include your API key in the request header:

Authorization: Bearer YOUR_API_KEY

> Get started in minutes with free SMS credits. No credit card required.

---

### 📤 Request

```json
{
  "AccountID": "YOUR_ACCOUNT_ID",
  "To": "27828703205",
  "MessageText": "Test from Gurrom Flow"
}
```

---

### 📥 Response

```json
{
  "isSuccess": true,
  "messageStatus": "SUCCESS",
  "messageTrackingNumber": "3727691",
  "creditsAvailable": 76825
}
```

---

💡 That’s it — your SMS is sent.

---

## 🧪 Code Examples

### C# (.NET)

```csharp
using System.Net.Http;
using System.Text;
using System.Threading.Tasks;

var client = new HttpClient();

client.DefaultRequestHeaders.Authorization = 
    new System.Net.Http.Headers.AuthenticationHeaderValue("Bearer", "YOUR_API_KEY");

var json = @"{
  ""AccountID"": ""YOUR_ACCOUNT_ID"",
  ""To"": ""27828703205"",
  ""MessageText"": ""Test from Gurrom Flow""
}";

var content = new StringContent(json, Encoding.UTF8, "application/json");

var response = await client.PostAsync(
    "https://api.flow.gurrom.co.za/api/messageapi/sendmessage",
    content
);

var result = await response.Content.ReadAsStringAsync();
Console.WriteLine(result);
```

---

### Node.js

```javascript
const axios = require('axios');

axios.post(
    'https://api.flow.gurrom.co.za/api/messageapi/sendmessage',
    {
        AccountID: "YOUR_ACCOUNT_ID",
        To: "27828703205",
        MessageText: "Test from Gurrom Flow"
    },
    {
        headers: {
            Authorization: "Bearer YOUR_API_KEY"
        }
    }
)
.then(res => console.log(res.data))
.catch(err => console.error(err));
```

---

### Python

```python
import requests

response = requests.post(
    "https://api.flow.gurrom.co.za/api/messageapi/sendmessage",
    json={
        "AccountID": "YOUR_ACCOUNT_ID",
        "To": "27828703205",
        "MessageText": "Test from Gurrom Flow"
    },
    headers={
        "Authorization": "Bearer YOUR_API_KEY"
    }
)

print(response.json())
```

---

## 📦 Postman Collection

Import the collection to get started instantly:

[![Run in Postman](https://run.pstmn.io/button.svg)](https://github.com/gurrom/gurrom-flow-api/blob/main/gurrom_flow_api_postman_collection.json)

Import into Postman:
1. Open Postman
2. Click "Import"
3. Select the JSON file
4. Set your API key and account ID
   
---

## 📖 API Details

| Field        | Type   | Description |
|-------------|--------|-------------|
| AccountID   | string | Your account identifier |
| To          | string | Recipient number in international format (e.g. 2782...) |
| MessageText | string | SMS message content |

---

## 📊 Response Fields

| Field                  | Description |
|-----------------------|------------|
| isSuccess             | Indicates success |
| messageStatus         | Status of the message |
| messageTrackingNumber | Unique message ID |
| creditsAvailable      | Remaining SMS credits |

---

## 🚀 Use Cases

- OTP / verification messages  
- Transactional alerts  
- System notifications  
- Customer communication  
- Billing reminders  

---

## 🌍 Why Gurrom Flow?

- 🇿🇦 Optimised for South African delivery
- ⚡ Simple REST API (no complexity)
- 💰 Cost-effective vs global providers
- 🔌 Built for integration into existing systems

---

## 🔜 Coming Soon

- WhatsApp API  
- Email API  
- Messaging workflows & automation  
- Webhooks & delivery tracking  

---

## 🚀 Get Access

👉 https://flow-gurrom.figma.site/  
👉 support@gurrom.co.za  

---

## 🔍 Keywords

SMS API South Africa  
Send SMS via API  
Transactional SMS API  
Bulk SMS API  
Messaging API REST  
WhatsApp API (coming soon)
