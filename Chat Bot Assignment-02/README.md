# Chatbot for CDP Documentation

## Overview

This project is a chatbot designed to assist users with queries related to four Customer Data Platform (CDP) documentations: **Segment, mParticle, Lytics, and Zeotap**. The chatbot retrieves relevant information from these documentations to provide accurate responses.

### Source Acknowledgment

This project is adapted from [Hitank Shah's Chatbot for CDP Documentation](https://github.com/hitankshah/Chatbot-for-CDP-Documentation-). The implementation has been modified and extended to meet specific requirements.

## Requirements

Ensure you have the following dependencies installed before running the project:

- Python 3.7 or higher
- pip (Python package installer)
- Flask
- BeautifulSoup4
- requests
- sentence-transformers
- PyTorch

## Installation Steps

1. **Clone the Repository**

   ```sh
   git clone https://github.com/hitankshah/Chatbot-for-CDP-Documentation-
   cd Chatbot-for-CDP-Documentation-
   ```

2. **Create a Virtual Environment (Recommended)**

   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Upgrade pip**

   ```sh
   python -m pip install --upgrade pip
   ```

4. **Install Dependencies**

   ```sh
   pip install flask beautifulsoup4 requests sentence-transformers torch==2.4.1 torchvision==0.19.1
   ```

   *Or install from requirements file:*

   ```sh
   pip install -r requirements.txt
   ```

5. **Run the Application**

   ```sh
   python app.py
   ```

   The application will be accessible at [**http://localhost:5000**](http://localhost:5000).

## Configuration

The chatbot retrieves documentation from the following URLs:

- **Segment**: [https://segment.com/docs/?ref=nav](https://segment.com/docs/?ref=nav)
- **mParticle**: [https://docs.mparticle.com/](https://docs.mparticle.com/)
- **Lytics**: [https://docs.lytics.com/](https://docs.lytics.com/)
- **Zeotap**: [https://docs.zeotap.com/home/en-us](https://docs.zeotap.com/home/en-us)

## Usage

### UI Access

Visit [**http://localhost:5000**](http://localhost:5000) to interact with the chatbot.

### API Endpoint

You can also make a **POST request** to `/ask` with a JSON payload containing the user's query.

#### Example Queries

- *"How do I set up a new source in Segment?"*
- *"How can I create a user profile in mParticle?"*
- *"How do I build an audience segment in Lytics?"*
- *"How can I integrate my data with Zeotap?"*

## Features

### Handling Variations

The chatbot can process different phrasings of the same question and provide accurate responses based on the relevant CDP documentation.

### Advanced Capabilities

- **Cross-CDP Comparisons**: It can compare features across different CDPs, e.g., *"How does Segment's audience creation process compare to Lytics'?"*
- **Complex Queries**: Supports advanced questions regarding configurations and integrations.

## Implementation Details

### Tech Stack

- **Programming Language**: Python
- **Framework**: Flask for backend API
- **NLP Libraries**: Sentence-Transformers for semantic understanding
- **Web Scraping**: BeautifulSoup4 and Requests for fetching documentation data
- **Deep Learning Framework**: PyTorch for processing queries with sentence embeddings

### Data Structures Used

- **Trie**: For efficiently storing and searching frequently asked questions
- **HashMaps**: Used for quick lookups of documentation content
- **Embedding-based Search**: Converts user queries and documentation into vector representations for similarity matching

### Deployment Strategy

- **Local Deployment**: Runs on `http://localhost:5000` during development
- **Cloud Deployment (Optional)**: Can be deployed to cloud services like AWS, Heroku, or GCP for broader access
- **Docker Support (Future Enhancement)**: Containerizing the application for consistent deployment environments

## Troubleshooting

- **ModuleNotFoundError**: Ensure all dependencies are installed correctly. Try reinstalling `pip` or the required packages.
- **Version Conflicts**: If experiencing compatibility issues with `torch` and `torchvision`, verify the installed versions match the recommended ones.

## License

This project is licensed under the MIT License. See the LICENSE file for details.

