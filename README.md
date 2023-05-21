# RCA of Production Crashes Presentation

This project aims to develop a software tool that presents the root cause analysis (RCA) of production crashes to non-technical clients in an easy-to-understand format. The tool fetches data related to production crashes through various APIs, analyses the data using NLP techniques to determine the crash's root cause, and presents this information to clients via a Flask web application.

## Technical Requirements

- Python 3.6 and above
- Flask web framework
- SQLAlchemy ORM
- TextBlob for natural language processing and analysis
- APIs like JIRA, Jenkins, Github, etc. to fetch data related to production crashes

## Setup

1. Clone the repository from GitHub.
2. Install the dependencies using the command `pip install -r requirements.txt`.
3. Configure the database details in the `.env` file.
4. Run the Flask web application using the command `python app.py`.
5. Visit the web application at `http://localhost:5000`.

## Usage

1. Use the "Summary" text area to provide a brief summary of the production crash. This summary should include the following fields:
   - **Title**: a short title describing the problem encountered.
   - **Description**: a detailed account of the issue, including details such as how long it has existed, what systems it affects, how it is triggered, and any other relevant details.
   - **Priority**: a rating of the priority of the issue, ranging from low to high.

2. Click the "Submit" button to fetch data related to the production crash from various APIs.
3. The fetched data will be pre-processed and analyzed using NLP techniques, such as bag of words, cosine similarity, text classification, etc.
4. The root cause analysis of the production crash will be displayed in an easy-to-understand format, including possible solutions and next steps.

## File Architecture
```
RCA-of-Production-Crashes-Presentation
|   app.py                                  # python script to run flask web application
|   requirements.txt                        # dependencies required for the project
|   README.md                               # Project ReadMe
|   .env.example                            # example environment variables
|   .gitignore                              # files for Git to ignore
|   LICENSE                                 # project license information

\---templates
│   │   index.html                          # HTML template for homepage
```

This file architecture was chosen due to the project's simplicity and modularity. The root directory contains the `app.py` script that serves as the entry point for running the Flask web application. It also contains other basic files like the `.env.example`, `.gitignore`, and the `LICENSE`. The `templates` directory contains the HTML template used to display the application's output. This architecture allows for easy setup of the project and modifications of the HTML interface, which is the primary purpose of the application.

## Conclusion

This project aimed to provide a technical solution for presenting root cause analysis of production crashes to non-technical clients. With the use of various APIs, NLP techniques, and the Flask web framework, the tool can fetch, analyze and present data in an easy-to-understand format. The detailed README and file architecture will enable other developers to understand and set up the project with ease.
