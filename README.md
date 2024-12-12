# SentimentCSVClassifier

This project is a **Sentiment CSV Classifier** application built with Streamlit. The app allows users to upload a CSV file containing textual data, perform sentiment analysis on the text using OpenAI's GPT model via the `scikit-llm` library, and download the results.

# What is Zero-shot classification ?

Zero-shot classification refers to the ability of a machine learning model to correctly classify data instances from classes that it has never encountered during training. Essentially, it can generalize its understanding to new, unseen categories without requiring additional training on those specific categories.

## Features
- **Upload CSV**: Users can upload CSV files for analysis.
- **Sentiment Analysis**: The app uses GPT-4 for zero-shot sentiment classification.
- **Result Display**: Outputs a dataframe with the original data and corresponding sentiment labels.
- **Download Results**: Provides an option to download the processed CSV file with sentiment labels.

## Requirements
The following Python libraries are required:

```plaintext
scikit-llm
streamlit
python-dotenv
pandas
```

## Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```

2. **Install Dependencies**
   Install the required Python libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. **Configure Environment Variables**
   Create a `.env` file in the root directory and add your OpenAI API key and organization name:
   ```dotenv
   OPENAI_API_KEY=your_openai_api_key
   ORGANIZATION_NAME=your_organization_name
   ```

4. **Run the Application**
   Start the Streamlit application:
   ```bash
   streamlit run app.py
   ```

5. **Upload and Analyze CSV**
   - Upload a CSV file with a `Review` column.
   - Click the **Analyze CSV File** button to process the file.
   - View the results and download the updated CSV.

## File Structure
```plaintext
.
├── app.py               # Main application file
├── requirements.txt     # Dependency file
├── .env                 # Environment variables
└── README.md            # Project documentation
```

## Usage
1. Upload a CSV file with a `Review` column containing text data.
2. Click on **Analyze CSV File**.
3. View the dataframe with an added `Sentiment` column.
4. Download the processed CSV by clicking the **Download data as CSV** button.

## Example Input CSV
| Review              |
|---------------------|
| I love this product |
| This is terrible    |

## Example Output CSV
| Review              | Sentiment    |
|---------------------|--------------|
| I love this product | Positive     |
| This is terrible    | Negative     |

## Technologies Used
- **Streamlit**: For building the web interface.
- **scikit-llm**: For integrating OpenAI's GPT model for sentiment classification.
- **Pandas**: For data manipulation and analysis.
- **Python-dotenv**: For managing environment variables.

## License
This project is licensed under the MIT License.

## Acknowledgements
- [Streamlit](https://streamlit.io/)
- [OpenAI](https://openai.com/)
- [scikit-llm](https://github.com/scikit-llm)