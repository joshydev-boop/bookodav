
# Booko-DAV - Self-Deployable WebDAV for eBook Management

[![Deploy to Cloudflare Workers](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/Joshuajrodrigues/bookodav)

## Features
 
- 10GB free storage tier with R2  
- Native KOReader WebDAV compatibility  
- Basic authentication protection  
- Serverless architecture with minimal maintenance  
- Cross-platform WebDAV client support  

## Dashboard
![Screenshot 2025-03-01 at 15-01-01 BOOKO-DAV - Instructions](https://github.com/user-attachments/assets/92c9f242-6e8a-4236-b9a0-45b1a77cc3b6)
![Screenshot 2025-03-01 at 15-01-17 BOOKO-DAV - Upload](https://github.com/user-attachments/assets/5f02ea04-4d8b-4d92-bde3-6387acb16209)
![Screenshot 2025-03-01 at 15-01-30 BOOKO-DAV - List](https://github.com/user-attachments/assets/18288766-1395-4851-9bb5-c7d516160959)



## Implementation Overview

```plaintext
┌─────────────┐        ┌──────────────┐        ┌─────────────┐
│   Client    │ HTTP   │ Cloudflare   │  R2 API │  R2 Storage │
│ (KOReader)  │◄──────►│   Worker     │◄───────►│  (bookodav) │
└─────────────┘        └──────────────┘        └─────────────┘
```

## Setup

1. Create Cloudflare R2 bucket named `bookodav`  
2. Deploy worker bookodav-worker with required environment variables:  
   - `USERNAME`: Authentication username  
   - `PASSWORD`: Authentication password  


## Integration

KOReader Configuration:

```yaml
WebDAV:
  URL: https://[worker-subdomain].workers.dev
  Username: [your-username]
  Password: [your-password]
```
## Cost Structure (Cloudflare)

| Service         | Free Tier       | Paid Tier          |
|-----------------|-----------------|--------------------|
| R2 Storage      | 10GB            | $0.015/GB-month    |
| Requests        | 100,000/day     | $0.15/million      |

## Development

Open to contributions and new features.
Contributions must maintain GPL-3.0 compliance. 


instructions
![Screenshot 2025-04-23 000023](https://github.com/user-attachments/assets/eeefd3e7-e0ca-4a65-8332-1288ec077e07)
![Screenshot 2025-04-23 000214](https://github.com/user-attachments/assets/059b7509-ac95-4242-8ceb-db1e40082986)
![image](https://github.com/user-attachments/assets/4a631ac5-3282-4855-9732-2d5c17d478fc)

![Screenshot 2025-04-23 002507](https://github.com/user-attachments/assets/b3937a58-ebf3-4e57-b931-db0fef95d7be)
![Screenshot 2025-04-23 002632](https://github.com/user-attachments/assets/066efc60-ed9d-40c4-86f4-c7c027664054)
![Screenshot 2025-04-23 002655](https://github.com/user-attachments/assets/9a452c07-16c4-4357-8a72-5bd6a14187c1)
![Screenshot 2025-04-23 002741](https://github.com/user-attachments/assets/a0e1986a-84b8-499c-8297-8e6a9b707675)
![Screenshot 2025-04-23 002806](https://github.com/user-attachments/assets/cbf74b3c-2ca8-453e-ac05-6892798bf1bc)
![Screenshot 2025-04-23 002855](https://github.com/user-attachments/assets/797ce986-f421-43c7-a0d6-05e826d3f2e1)
![Screenshot 2025-04-23 004847](https://github.com/user-attachments/assets/dea5b807-f84e-429c-a83f-dfadcba89b9b)
![Screenshot 2025-04-23 004933](https://github.com/user-attachments/assets/6d2fcdd2-313e-47ee-bab1-81708217767e)




