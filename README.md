# Intenship-Assignment
# Get Papers List

A command-line tool to fetch research papers from PubMed based on a user-specified query. This tool allows filtering results to identify papers with non-academic authors affiliated with pharmaceutical or biotech companies, and outputs the data as a CSV file.

## Features
- Fetch papers using the PubMed API with full query syntax support.
- Extract detailed information including:
  - PubMed ID
  - Title
  - Publication Date
  - Non-academic authors
  - Company affiliations
  - Corresponding author email
- Output results to a CSV file or the console.
- Command-line options for flexible usage.

## Installation

### Prerequisites
- Python 3.8 or higher
- Poetry for dependency management

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/get-papers-list.git
   cd get-papers-list
   ```

2. Install dependencies using Poetry:
   ```bash
   poetry install
   ```

3. Activate the virtual environment:
   ```bash
   poetry shell
   ```

## Usage

### Command
Run the tool using the `get-papers-list` command:
```bash
get-papers-list "<search-query>" [options]
```

### Options
- `-h, --help`: Display usage instructions.
- `-d, --debug`: Print debug information during execution.
- `-f, --file <filename>`: Specify the filename to save results. If not provided, the output is printed to the console.

### Examples
1. Fetch papers and print results to the console:
   ```bash
   get-papers-list "COVID-19 vaccine"
   ```

2. Fetch papers and save results to `results.csv`:
   ```bash
   get-papers-list "genetic therapy" -f results.csv
   ```

3. Enable debug mode:
   ```bash
   get-papers-list "antiviral drugs" -d
   ```

## Project Structure
- `fetch_research_papers.py`: Main script containing the program logic.
- `pyproject.toml`: Poetry configuration file for dependencies and packaging.
- `README.md`: Documentation for the project.

## Development

### Adding Dependencies
To add a new dependency, use Poetry:
```bash
poetry add <package-name>
```

### Running Locally
1. Ensure you are in the Poetry environment:
   ```bash
   poetry shell
   ```
2. Run the script:
   ```bash
   python fetch_research_papers.py "<search-query>"
   ```

## Contributing
1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature-name
   ```
3. Commit changes:
   ```bash
   git commit -m "Description of changes"
   ```
4. Push to your fork:
   ```bash
   git push origin feature-name
   ```
5. Create a pull request.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments
- [PubMed API Documentation](https://www.ncbi.nlm.nih.gov/home/develop/api/)
- [Poetry Documentation](https://python-poetry.org/docs/)

