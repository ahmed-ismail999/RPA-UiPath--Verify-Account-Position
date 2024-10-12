# RPA - Verify Account Position

## Project Overview

**Verify Account Position** is an RPA project designed to automate the reconciliation process between ACME System 1 and ACME System 3. The project involves logging into both systems using credentials stored in Orchestrator assets, extracting work item details from ACME System 1, and comparing account movement totals from ACME System 3. The results are uploaded to the Orchestrator queue and used to update work item details in ACME System 1, ensuring data consistency across both platforms.

## Features

- **ACME System 1 Login**: Automatically logs into ACME System 1 using credentials retrieved from Orchestrator assets.
- **ACME System 3 Login**: Logs into ACME System 3 on the user's device with the same credentials.
- **Work Items Extraction**: Reads and extracts work items from the work items table in ACME System 1.
- **Dispatcher Workflow**: Uploads extracted work items to the Orchestrator queue using the dispatcher workflow.
- **Account Movements Extraction**: Extracts account movements from ACME System 3 for reconciliation.
- **Data Comparison**: Compares account movements from ACME System 3 with account amounts in ACME System 1.
- **Work Item Updates**: Updates the work item details in ACME System 1 based on the comparison results.

## Technology Stack

- **UiPath RPA Framework**: Used for automating the workflow between ACME System 1 and ACME System 3.
- **Orchestrator**: Manages the credentials and queues for the work item extraction and comparison processes.
- **ACME System 1 & 3**: External systems for account management and processing.

## Workflow Breakdown

1. **Login to ACME System 1**  
   - The bot launches ACME System 1 and retrieves user credentials from the Orchestrator.
   - The bot logs into the system to access work items.
   
2. **Login to ACME System 3**  
   - The bot launches ACME System 3 on the user’s device.
   - The bot logs into the system using the same credentials retrieved from the Orchestrator.
   
3. **Dispatcher Workflow**  
   - The bot extracts work items from ACME System 1, including necessary details like account numbers, amounts, and transaction IDs.
   - The extracted data is uploaded to the Orchestrator queue.
   
4. **Account Reconciliation**  
   - The bot extracts account movement totals from ACME System 3.
   - It compares these totals with the account amounts in ACME System 1 to check for discrepancies.
   
5. **Work Item Updates**  
   - Based on the comparison results, the bot updates the relevant work item details in ACME System 1.
   
