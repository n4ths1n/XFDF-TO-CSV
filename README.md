
# XFDF to CSV Converter

## Description

This script transforms form data received via email in `.xfdf` format and converts it into a structured and ordered `.csv` file. It is useful for processing digitally completed forms, exporting data into a manageable format, and automating the handling of large volumes of information.

## Features

- Reads `.xfdf` files containing form data.
- Extracts and organizes the information into specific columns.
- Exports the organized data into a `.csv` file for analysis or integration with other systems.

## Prerequisites

To use this script, make sure you have the following:

1. Python 3.x installed on your system.
2. The following Python libraries installed:
   - `pandas`
   - `lxml`

You can install them by running:

```bash
pip install pandas lxml
```

## Usage

1. Place your `.xfdf` files in the same directory as the script or specify the file path when running it.
2. Run the script from the terminal or command line with the following command:

```bash
python xfdf_to_csv.py input.xfdf output.csv
```

   - **`input.xfdf`**: The XFDF file you want to process.
   - **`output.csv`**: The name of the generated CSV file.

3. The generated CSV file will be ready in the specified location.

## Example

### Input XFDF File:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<xfdf xmlns="http://ns.adobe.com/xfdf/" xml:space="preserve">
    <fields>
        <field name="name">
            <value>John Doe</value>
        </field>
        <field name="email">
            <value>john.doe@example.com</value>
        </field>
        <field name="comments">
            <value>Excellent service.</value>
        </field>
    </fields>
</xfdf>
```

### Output CSV File:

```csv
name,email,comments
John Doe,john.doe@example.com,Excellent service.
```

## Notes

- The script is designed to handle standard text fields in XFDF forms.
- Ensure your XFDF files are well-formed and adhere to the Adobe XFDF standard.

## Customization

If you need to adjust the script for specific fields or custom formats, you can directly edit it in the sections where the XFDF structure is processed.

## Contributions

If you'd like to improve this script, feel free to fork it or submit a pull request in the associated repository.
