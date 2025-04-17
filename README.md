- 👋 Hi, I’m @caoruiR
- 👀 I’m interested in hush
- 🌱 I’m currently learning manbo
- 💞️ I’m looking to collaborate on don't speak
- 📫 How to reach me wow
- 😄 Pronouns: 
- ⚡ Fun fact: 

erDiagram
    USER ||--o{ USER : created_by
    SYS_USER ||--|| USER : sys_user_id

    USER {
        bigint id PK
        datetime created_at
        datetime updated_at
        datetime deleted_at
        varchar uid
        varchar image_url
        varchar identify_result
        bigint created_by FK
    }
    SYS_USER {
        bigint id PK
        datetime created_at
        datetime updated_at
        datetime deleted_at
        varchar customer_name
        varchar customer_phone
        bigint sys_user_id FK
        bigint sys_user_pwd
    }
    JWT {
        bigint id PK
        datetime created_at
        datetime updated_at
        datetime deleted_at
        text jwt
    }
    RETENTION_FILE {
        bigint id PK
        datetime created_at
        datetime updated_at
        datetime deleted_at
        varchar file_name
        varchar file_path
        bigint chunk_total
    }

<!---
caoruiR/caoruiR is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
