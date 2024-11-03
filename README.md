# SafeScan

SafeScan is an innovative platform that empowers users to make informed decisions about beauty products, medications, and packaged foods. By simply uploading a photo of any product label, our advanced AI technology analyzes the ingredients for toxic substances, harmful allergens, and potential side effects, delivering a detailed safety rating and risk report.

## Links

- https://safescan.tech
- https://isitsafeforme.tech

## Features

- **Product Recognition**: Uses Google Cloud Vision API to identify products from images.
- **Ingredient Analysis**: Analyzes ingredients for toxic substances and harmful allergens.
- **Safety Reports**: Provides detailed safety ratings and risk reports.
- **Google Search Integration**: Fetches relevant product information from Google search results.
- **Streamlit Interface**: User-friendly interface built with Streamlit.

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/safescan.git
    cd safescan
    ```

2. Install the required dependencies:
    ```sh
    pip install -r application/requirements.txt
    ```

3. Set up Google Cloud Vision API credentials:
    - Place your `service_account.json` file in the `application` directory.

4. Add your OpenAI API key and SAPAPI API key in `agent.py`:
    ```python
    # agent.py
    openai_api_key = 'your_openai_api_key'
    sapapi_api_key = 'your_sapapi_api_key'
    ```

5. Add information about your Cloudflare and AWS account in `worker.js` and `main.tf`:
    ```javascript
    // worker.js
    const cloudflareAccount = 'your_cloudflare_account_info';
    const awsAccount = 'your_aws_account_info';
    ```

    ```hcl
    # main.tf
    provider "aws" {
      access_key = "your_aws_access_key"
      secret_key = "your_aws_secret_key"
      region     = "your_aws_region"
    }

    resource "cloudflare_record" "example" {
      zone_id = "your_cloudflare_zone_id"
      name    = "example"
      value   = "your_cloudflare_value"
      type    = "A"
    }
    ```

6. Run the application:
    ```sh
    streamlit run application/index.py
    ```

## Usage

1. Open the application in your web browser.
2. Upload an image of a product label.
3. View the detailed safety report generated by the application.

## Project Structure
├── .gitignore 
├── .terraform
├── application/ 
    ├── agent.py 
    ├── Dockerfile
    ├── index.py
    ├── main.tf 
    ├── requirements.txt 
├── README.md 
└── worker/ 
    ├── main.tf 
    └── worker/worker.js

