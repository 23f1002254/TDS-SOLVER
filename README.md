# TDS-SOLVER
A smart API that automatically solves graded assignments for IIT Madras' Tools in Data Science course. Submit any question from the five graded assignments with optional file attachments, and receive the correct answer in JSON format ready for submission.
# Assignment Solver API

An intelligent API service that automatically solves graded assignments for the Tools in Data Science course in the IIT Madras Online Degree in Data Science program.

## Features

- Handles questions from all five graded assignments
- Processes attached files (CSV, ZIP, etc.)
- Returns answers in submission-ready format
- Simple API interface for easy integration

## API Usage

The API endpoint accepts POST requests with multipart/form-data containing:
- The assignment question
- Any necessary file attachments

### Endpoint
POST https://your-app.vercel.app/api/
### Request Format
```bash
curl -X POST "https://your-app.vercel.app/api/"
-H "Content-Type: multipart/form-data"
-F "question=Download and unzip file abcd.zip which has a single extract.csv file inside. What is the value in the "answer" column of the CSV file?"
-F "file=@abcd.zip"
```

### Response Format
```json
{
"answer": "1234567890"
}
```

## Implementation
#### The API is built using:
- Next.js API routes for the backend
- Language model for question understanding and answer generation
- File processing utilities for handling various data formats

## Setup and Deployment
1. Clone this repository
2. Install dependencies with `npm install`
3. Configure your environment variables
4. Deploy to Vercel or your preferred hosting platform

## Limitations
This tool is designed for educational purposes only. Please use responsibly and in accordance with your institution's academic integrity policies.
## License
MIT

