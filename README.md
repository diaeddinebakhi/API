# API

# Introduction to APIs
An API (Application Programming Interface) is a way for different software applications to communicate and share data. APIs work as a bridge, allowing one program to request specific information or actions from another program.


## What is an API?
An API defines a set of rules and protocols for accessing and exchanging data between software applications. It enables developers to integrate external services and functions without building them from scratch.

### Key Terminology
- **Client**: The software making the request (e.g., a mobile app).
- **Server**: The system providing the API and handling requests.
- **Endpoint**: A specific URL where an API listens for requests.
- **Request/Response**: The process of sending and receiving data from an API.


## Common API Request Types
APIs use specific request methods to perform different actions. The most common methods are:

- **GET**: Retrieve data.
- **POST**: Send data to the server.
- **PUT**: Update existing data.
- **DELETE**: Remove data.


## Example API Usage: OpenWeatherMap
Let's use the OpenWeatherMap API to retrieve current weather data for a specific city.

To follow along, you'll need an API key from OpenWeatherMap (or another weather API of your choice).

### Step 1: Get an API Key
1. Go to [OpenWeatherMap](https://openweathermap.org/).
2. Sign up for a free account and log in.
3. Go to the **API keys** section in your profile, and click **Generate** or **Create New Key**.
4. Copy the API key and store it securely (do not share it publicly).

### Step 2: Install the `requests` Library
We'll use the `requests` library in Python to send HTTP requests to the API. If you don't already have it, install it by running:

```python
!pip install requests


```markdown
## Making an API Call
Below is the code to fetch current weather data for a city using the OpenWeatherMap API.
Replace `"your_api_key"` with the API key you obtained in Step 1.
you can see code "weather_api.ipynb"


## Explanation of the Code
1. **API URL**: `base_url` is the URL endpoint with parameters for city, API key, and units (Celsius).
2. **Sending the Request**: `requests.get(base_url)` sends a GET request to the API.
3. **Status Check**: `response.status_code` verifies if the request was successful (200 indicates success).
4. **Parsing JSON**: `response.json()` converts JSON data into a Python dictionary.
5. **Extracting Data**: Specific weather information (temperature, humidity) is retrieved and printed.
```

## Additional API Tips
- **API Rate Limits**: APIs may limit requests per minute or day. Always check the provider's limits.
- **Error Handling**: Check response codes to handle errors gracefully.
- **Environment Variables**: Store sensitive data like API keys in environment variables instead of hardcoding them.



# Conclusion
APIs enable seamless data exchange between applications, allowing developers to integrate powerful features from external services. By understanding API requests and responses, you can add valuable functionality to your applications.
