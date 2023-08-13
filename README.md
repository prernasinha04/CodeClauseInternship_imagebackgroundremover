# CodeClauseInternship_imagebackgroundremover
import requests

def remove_background(image_path, api_key):
    api_url = "https://api.remove.bg/v1.0/removebg"
    files = {'image_file': open(image_path, 'rb')}
    headers = {'X-Api-Key': api_key}
    response = requests.post(api_url, files=files, headers=headers)

    if response.status_code == 200:
        with open('output.png', 'wb') as output_file:
            output_file.write(response.content)
        print("Background removed and saved as 'output.png'")
    else:
        print("Error:", response.status_code)

# Replace with your API key
api_key = 'EWpofC9VzLJSqKtbCvpBPEGv'
image_path = 'images.jpeg'

remove_background(image_path, api_key)
