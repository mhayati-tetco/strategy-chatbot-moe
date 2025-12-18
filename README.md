# strategy-chatbot-moe

- to be added or changed:

1. python services for fallbacks

2. after receiving the data, apply preprocessing

3. update the front-end to display the correct time stamp

Database Structure:

chat_header
| Column Name | Type    | Key         |
| ----------- | ------- | ----------- |
| session_id  | varchar | Primary Key |
| chat_header | varchar | —           |
| user_id     | varchar | —           |

n8n_chat_histories
| Column Name | Type    | Key         |
| ----------- | ------- | ----------- |
| id          | int4    | Primary Key |
| session_id  | varchar | —           |
| message     | jsonb   | —           |

user_chat_history
| Column Name | Type        | Key                       |
| ----------- | ----------- | ------------------------- |
| session_id  | varchar     | —                         |
| u_id        | varchar     | Foreign Key → users(u_id) |
| message     | jsonb       | —                         |
| time        | timestamptz | —                         |

users
| Column Name | Type    | Key         |
| ----------- | ------- | ----------- |
| u_id        | varchar | Primary Key |
| email       | varchar | —           |
| full_name   | varchar | —           |
| password    | varchar | —           |


Note:
- please update the webpage design just make it look better
