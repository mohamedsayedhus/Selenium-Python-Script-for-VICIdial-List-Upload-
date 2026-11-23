# VICIdial List Automation

Python and Selenium example for list creation, file uploads and field mapping in a VICIdial administration interface.

## Purpose

Reduce repetitive browser interaction when configuring multiple lists. The notebook iterates through list IDs, creates list entries, uploads files and maps fields through the web interface.

This is a portfolio example, not a claim of measured time savings or a production-ready integration.

## Tools

Python, Selenium, Chrome WebDriver and PyAutoGUI.

## Included files

- `Selenium_.ipynb`: automation notebook.
- `.env.example`: configuration names with non-working example values.
- `.gitignore`: excludes local credentials, lead files and generated outputs.
- `README.md`: setup, safety and limitations.

## Configuration

Install Jupyter, Selenium and PyAutoGUI in a local Python environment. Configure a compatible Chrome/ChromeDriver installation. Copy the variable names from `.env.example` into your local process environment; the example file is not loaded automatically.

Required environment variables:

- `VICIDIAL_BASE_URL`: authorized test-instance administration URL.
- `VICIDIAL_USERNAME` and `VICIDIAL_PASSWORD`: local login values, never committed.
- `VICIDIAL_FILE_PATTERN`: local upload-path pattern, using `{}` for date prefix and part index.

Set the list IDs, list names and campaign selection for an authorized test environment. Review every selector and field mapping before running.

## Safety

This notebook makes changes on the target system and uploads lead data. It has no dry-run mode or rollback. Use only a test instance and synthetic lead files until the workflow has been checked. Do not upload customer data, credentials, private endpoints or captured error screenshots to GitHub.

## Limitations

- Selectors and campaign settings are specific to the original interface and may need changes.
- PyAutoGUI types into the active window, so focus and timing matter.
- Some waits are fixed delays.
- The example needs local configuration and has not been runtime-tested as part of this documentation update.
- Removing a value from the current notebook does not erase previous commits. Any exposed credential must be rotated independently; history cleanup is a separate operation.
