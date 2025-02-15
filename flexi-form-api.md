# Flexi API Documentation

## Authentication
Base endpoint: `/flexi`

### User Authentication

| Method | Endpoint | Description | Authentication Required |
|--------|----------|-------------|------------------------|
| POST | `/login` | Log in to the system | No |
| POST | `/register` | Register a new user | No |
| GET | `/current-user` | Get current user information | Yes |
| POST | `/update-profile` | Update user profile | Yes |
| POST | `/logout` | Log out from the system | Yes |

### User Management

| Method | Endpoint | Description | Authentication Required |
|--------|----------|-------------|------------------------|
| GET | `/users` | Get all users | Yes |
| POST | `/users` | Create new user | Yes |
| PUT | `/users/:id` | Update user by ID | Yes |
| DELETE | `/users/:id` | Delete user by ID | Yes |
| GET | `/users/:id` | Get user by ID | Yes |

## Form Responses

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/form-responses` | Get all form responses |
| GET | `/form-responses/:id` | Get form response by ID |
| POST | `/form-responses` | Create new form response |
| PUT | `/form-responses/:id` | Update form response |
| DELETE | `/form-responses/:id` | Delete form response |
| GET | `/form-responses/stats/:form_id` | Get form response statistics |

## Form Settings

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/forms/:form_id/settings` | Get form settings |
| PUT | `/forms/:form_id/settings` | Update form settings |
| DELETE | `/forms/:form_id/settings` | Delete form settings |
| GET | `/forms/:form_id/accessibility` | Check form accessibility |

## Sections

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/forms/:form_id/sections` | Get all sections in a form |
| GET | `/sections/:id` | Get section by ID |
| POST | `/forms/:form_id/sections` | Create new section |
| PUT | `/sections/:id` | Update section |
| DELETE | `/sections/:id` | Delete section |

## Items

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/sections/:section_id/items` | Get all items in a section |
| GET | `/items/:id` | Get item by ID |
| POST | `/sections/:section_id/items` | Create new item |
| PATCH | `/items/:id` | Update item |
| DELETE | `/items/:id` | Delete item |

## Options

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/items/:item_id/options` | Get all options for an item |
| GET | `/options/:id` | Get option by ID |
| POST | `/items/:item_id/options` | Create new option |
| PUT | `/options/:id` | Update option |
| DELETE | `/options/:id` | Delete option |

## Logic Conditions

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/items/:item_id/logic-conditions` | Get logic conditions for an item |
| GET | `/forms/:form_id/logic-conditions` | Get all logic conditions in a form |
| POST | `/logic-conditions` | Create new logic condition |
| PUT | `/logic-conditions/:id` | Update logic condition |
| DELETE | `/logic-conditions/:id` | Delete logic condition |

## Response Answers

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/responses/:response_id/answers` | Get all answers for a response |
| POST | `/responses/:response_id/answers` | Submit single answer |
| POST | `/responses/:response_id/bulk-answers` | Submit multiple answers |
| DELETE | `/answers/:id` | Delete answer |
| GET | `/forms/:form_id/response-stats` | Get response statistics |

## Response Logs

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/responses/:response_id/history` | Get response history |
| GET | `/responses/:response_id/items/:item_id/history` | Get item history |
| POST | `/response-logs` | Log answer change |
| GET | `/forms/:form_id/changes-summary` | Get changes summary |

---

### Notes:
1. All endpoints are prefixed with `/flexi`
2. Authentication is required for most endpoints except login and register
3. For endpoints requiring IDs, replace `:id`, `:form_id`, `:section_id`, `:item_id`, and `:response_id` with actual IDs
4. Response formats and required request bodies are not specified in this documentation
