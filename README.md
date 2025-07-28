# Day-21
import requests

city = input("Enter city: ")
url = f"http://api.openweathermap.org/data/2.5/weather?q={city}&appid=YOUR_API_KEY&units=metric"

res = requests.get(url)
if res.status_code == 200:
    data = res.json()
    print("Temperature:", data['main']['temp'], "°C")
else:
    print("City not found.")
