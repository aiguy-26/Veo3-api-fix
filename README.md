


# Working Python Script for Google VEO 3 on Vertex AI

This repository contains a working Python script to generate videos using Google's VEO 3 model via the Vertex AI API.

## The Problem

As of August 2025, the official Google Gemini API documentation for VEO 3 provides Python code snippets that do not work with the currently available libraries. The code samples result in a series of errors, including `ImportError: cannot import name 'genai'`, `AttributeError: ... has no attribute 'Client'`, and incorrect methods for downloading the final video file.

This script provides a fully functional alternative that correctly uses the `google-cloud-aiplatform` library.

## Prerequisites

1.  **Python Environment:** Python 3.9+
2.  **Google Cloud Project:** You must have a GCP project that has been approved for the VEO 3 preview.
3.  **Authentication:** You must have the Google Cloud CLI installed and authenticated. Run this command:
    ```bash
    gcloud auth application-default login
    ```

## How to Use

1.  Clone this repository:
    ```bash
    git clone [your-repo-url]
    ```
2.  Install the required Python library:
    ```bash
    pip install google-cloud-aiplatform
    ```
3.  Open the `generate_veo_video.py` script.
4.  Edit the configuration section at the top of the file to include your `PROJECT_ID`, `LOCATION`, and desired `PROMPT`.
5.  Run the script from your terminal:
    ```bash
    python generate_veo_video.py
    ```
Your video will be saved in the same directory with a unique, timestamped filename.
