# CSV Natural Language Query Tool

A web-based tool that allows you to upload CSV files and query them using natural language, powered by any Open AI API compatible LLM. Ask questions about your data in plain English and get SQL queries generated automatically, with results displayed in an intuitive interface.
<img width="1210" height="839" alt="image" src="https://github.com/user-attachments/assets/387f3260-0568-404e-b049-bb58df946da3" />
<img width="1169" height="695" alt="image" src="https://github.com/user-attachments/assets/c20f3424-94ce-415c-b368-e5a2ae4d88b1" />
<img width="1153" height="508" alt="image" src="https://github.com/user-attachments/assets/dd5c7db4-fc3a-459a-a93e-c414580fb7c1" />

## Features

- **📁 Drag & Drop CSV Upload**: Easy file uploading with visual feedback
- **🤖 Natural Language Queries**: Ask questions in plain English
- **🔍 AI-Powered SQL Generation**: Automatic conversion from natural language to SQL
- **📊 Interactive Results**: View query results in formatted tables
- **🌙 Dark/Light Theme**: Toggle between themes with persistent settings
- **⚙️ Flexible API Configuration**: Support for multiple AI models and endpoints
- **📋 Collapsible Sections**: Organized UI with expandable/collapsible sections
- **💾 Persistent Settings**: Saves your preferences and API configuration
- **📱 Responsive Design**: Works on desktop and mobile devices

## Demo

Try the tool with the included `demosales.csv` sample dataset containing sales data with columns for dates, clients, products, quantities, prices, and regions.

## Quick Start

1. Download or clone this repository
2. Open `csv-nlq-tool.html` in your web browser
3. Configure your API settings (see [API Configuration](#api-configuration))
4. Upload a CSV file
5. Start asking questions about your data!

## Example Queries

Once you've uploaded a CSV file, you can ask questions like:

- "Show me the top 5 highest sales"
- "What's the average price by region?"
- "Count how many orders were placed in 2024"
- "Find all customers from the East region"
- "Show total revenue by month"
- "Which salesperson has the highest total sales?"

## API Configuration

The tool supports multiple AI providers and models:

### OpenAI (Default)
- **Endpoint**: `https://api.openai.com/v1/chat/completions`
- **Models**: GPT-3.5 Turbo, GPT-4, GPT-4 Turbo
- **API Key**: Get from [OpenAI Platform](https://platform.openai.com/api-keys)

### Local Models
- **Llama 3.1 8B**: For local inference setups
- **Mixtral 8x7B**: For local inference setups
- **Custom Models**: Enter any model name for custom endpoints

### Other Providers
The tool works with any OpenAI-compatible API endpoint. Simply change the endpoint URL and model name.

## File Format Requirements

- **File Type**: CSV (.csv files only)
- **Headers**: First row should contain column names
- **Encoding**: UTF-8 recommended
- **Size**: No hard limit, but larger files may take longer to process

## Data Schema Detection

The tool automatically analyzes your CSV and detects:

- **Column Types**: TEXT, INTEGER, REAL, BOOLEAN, DATE
- **Nullable Fields**: Columns that contain empty values
- **Data Quality**: Basic validation and type inference

## SQL Query Engine

The built-in SQL executor supports:

- **SELECT**: Column selection and wildcard queries
- **WHERE**: Filtering with comparison operators (=, !=, >, <, >=, <=, LIKE)
- **GROUP BY**: Aggregation and grouping
- **ORDER BY**: Sorting (ASC/DESC)
- **LIMIT**: Result limiting
- **Aggregates**: COUNT, SUM, AVG functions

## Technical Details

### Dependencies
- **PapaParse**: CSV parsing library
- **Native JavaScript**: No framework dependencies
- **CSS Variables**: For theming support

### Architecture
- **Single File**: Complete application in one HTML file
- **Client-Side**: All processing happens in the browser
- **Modular Design**: Well-organized class-based structure

## Troubleshooting

### Common Issues

**Q: "API Error" when making queries**
- Check your API key is correct
- Verify the endpoint URL
- Ensure you have sufficient API credits

**Q: "Error parsing CSV" message**
- Ensure file is a valid CSV format
- Check for proper UTF-8 encoding
- Verify headers are in the first row

**Q: Query returns no results**
- Check column names are spelled correctly
- Verify data types match your query
- Try simpler queries first

**Q: Large files slow to load**
- Consider splitting large files
- Close other browser tabs to free memory

### Performance Tips

- Files with thousands of rows work well
- Complex queries may take a few seconds
- Use LIMIT clause for faster results on large datasets

## Support

For issues or questions:

1. Check the [Troubleshooting](#troubleshooting) section
2. Review your API configuration
3. Try with the sample CSV file
4. Open an issue on GitHub

## Acknowledgments

- **PapaParse**: Excellent CSV parsing library
