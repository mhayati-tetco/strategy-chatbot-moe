# strategy-chatbot-moe

- to be added or changed:

1. python services for fallbacks

2. after receiving the data, apply preprocessing

3. update the front-end to display the correct time stamp

Database Structure:
------------------------------------------------------------------------
- chat_header |
  - session_id |       Type: varchar (Primary key)
  - chat_header |      Type: varchar
  - user_id |          Type: varchar
------------------------------------------------------------------------
- n8n_chat_histories |
  - id |               Type: int4 (Primary key)
  - session_id |       Type: varchar
  - message |           Type: jsonb
------------------------------------------------------------------------
- user_chat_history
  - session_id |       Type: varchar
  - u_id |             Type: varchar (foreign key -> users)
  - message |          Type: jsonb
  - time |             Type: timestampz
------------------------------------------------------------------------
- users
  - u_id |             Type: varchar (Primary key)
  - email |            Type: varchar
  - full_name |        Type: varchar
  - password |         Type: varchar
------------------------------------------------------------------------

Note:
- please update the webpage design just make it look better
