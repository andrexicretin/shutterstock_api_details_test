from requests_oauthlib import OAuth2Session
from dotenv import load_dotenv
import os

load_dotenv()

client_id = os.getenv('CLIENT_ID')
client_secret = os.getenv('CLIENT_SECRET')
token = os.getenv('TOKEN')



image_id = '607073963'


image_details_endpoint_url = f'https://api.shutterstock.com/v2/images/{image_id}'
params = {
    "language": "pt",
    "fields": "data(id,description,assets/preview_1500/url)",
}

session = OAuth2Session()
session.headers['Authorization'] = f"Bearer {token} "

response = session.get(image_details_endpoint_url, params=params)



print(f"STATUS CODE : {response.status_code}")
print(f"STATUS TEXT : {response.text}")
