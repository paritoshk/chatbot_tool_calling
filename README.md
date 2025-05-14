# Chatbot Tool Calling Implementation

This project demonstrates the implementation of a chatbot that uses tool calling capabilities to interact with a customer support system. The chatbot is built using the Together AI API and can handle various customer service tasks like looking up user information, checking order status, and processing order cancellations.

## Features

- Customer information lookup by email, phone, or username
- Order status checking and management
- Order cancellation processing
- Interactive chat interface
- Tool calling implementation for backend operations
- Colored terminal output for better readability

## Prerequisites

- Python 3.10 or higher
- Together AI API key
- Required Python packages (see Installation section)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/paritoshk/chatbot_tool_calling.git
cd chatbot_tool_calling
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows, use: venv\Scripts\activate
```

3. Install required packages:
```bash
pip install together python-dotenv colorama
```

4. Create a `.env` file in the project root and add your Together AI API key:
```
TOGETHER_API_KEY=your_api_key_here
```

## Usage

The project includes several demonstration scripts:

1. Basic API Testing:
```python
from tool_call_learn import get_response

messages = [{"role": "user", "content": "What are some fun things to do in New York?"}]
response = get_response(messages)
print(response)
```

2. Customer Support Chat:
```python
from tool_call_learn import simple_jupyter_chat

# Start the interactive chat
simple_jupyter_chat()
```

3. Debug Message Flow:
```python
from tool_call_learn import debug_message_flow

# Run the debug flow to see how messages are processed
debug_message_flow()
```

## Project Structure

- `tool_call_learn.ipynb`: Main Jupyter notebook containing the implementation
- `.env`: Environment variables file (not tracked in git)
- `.gitignore`: Git ignore file
- `README.md`: This documentation file

## Available Tools

The chatbot has access to the following tools:

1. `get_user`: Look up user information by email, phone, or username
2. `get_order_by_id`: Retrieve order details using order ID
3. `get_customer_orders`: Get all orders for a specific customer
4. `cancel_order`: Process order cancellation requests

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Together AI for providing the API
- The open-source community for various tools and libraries used in this project 