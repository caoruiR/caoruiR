- 👋 Hi, I’m @caoruiR
- 👀 I’m interested in hush
- 🌱 I’m currently learning manbo
- 💞️ I’m looking to collaborate on don't speak
- 📫 How to reach me wow
- 😄 Pronouns: 
- ⚡ Fun fact: 

erDiagram
    USER {
        bigint id PK "主键"
        datetime created_at "创建时间"
        datetime updated_at "更新时间"
        datetime deleted_at "删除时间，可空"
        varchar uid "用户ID"
        varchar image_url "图片URL"
        varchar identify_result "识别结果"
        bigint created_by FK "创建者ID，引用User.id"
    }
    SYS_USER {
        bigint id PK "主键"
        datetime created_at "创建时间"
        datetime updated_at "更新时间"
        datetime deleted_at "删除时间，可空"
        varchar customer_name "客户姓名"
        varchar customer_phone "客户电话"
        bigint sys_user_id FK "系统用户ID，引用User.id"
        bigint sys_user_pwd "系统用户密码"
    }
    JWT {
        bigint id PK "主键"
        datetime created_at "创建时间"
        datetime updated_at "更新时间"
        datetime deleted_at "删除时间，可空"
        text jwt "JWT令牌"
    }
    RETENTION_FILE {
        bigint id PK "主键"
        datetime created_at "创建时间"
        datetime updated_at "更新时间"
        datetime deleted_at "删除时间，可空"
        varchar file_name "文件名"
        varchar file_path "文件路径"
        bigint chunk_total "分块总数"
    }

    USER ||--o{ USER : "created_by"
    SYS_USER ||--|| USER : "sys_user_id"

<!---
caoruiR/caoruiR is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
