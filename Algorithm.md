# The Algorithm

## High level version
    
1. Get industry the business is in, path(s) to folder(s) containing the documents and any data available to train on (e.g. table containing predefined suppliers & customers, industries and accounts).
2. Extract data from documents and store it in a dataframe. Make the data available in a human-readable and editable form.
3. Learn from the corrections.
4. Process the corrected data to produce whatever is requested (e.g. accounts, FS, VAT, Tax Return, etc.).
5. Take review.

## Details

- Industry the business is in
  - There should be a list of different industries from which the user can choose. This list includes Manufacturing, Finance, Retail, Construction, Research, Agriculture, Investment, Health, etc.
  - The user should be helped in deciding which industry to choose. For example, by giving them an idea of what companies in each industry do.
  - This is necessary to decide which costs are direct and which indirect. This helps in revenue recognition as well.
  - The AI should learn and tailor the results according to it.
- Documents' folders
  - At least one of the following folders are required:
    - Bank statements one
    - Invoices and receipts one
  - The folder containing invoices and receipts can be split into two folders.
  - The user should be asked whether the receipts and invoices have been split or are in one folder.
  - There can be an optional folder containing the data to learn from.
  - The user should be helped in structuring the folders via images and GIFs explaining what goes in each folder and what is optional.
- Training data
  - This can be in the form of a CSV with headings **description** (name of customer or supplier), **industry** and **account**.
  - A list should be provided containing industries, accounts and their respective codes in numerical form.
  - The industry and account columns must contain codes of industries and accounts from the provided list.
  - The learning process should occur before assigning industries and accounts to the descriptions extracted from the documents.
  - The user should be guided how to write the desciptions and what goes in each column. The descriptions should be similar to what the AI will extract from the documents.
- Data extraction
  - Latest technologies such as OCR, DL, etc. should be utilized to extract data from images, PDFs, CSVs, etc.
  - As much data should be extracted as possible. This includes:
    - date
    - time
    - company
    - description of products &/or services
    - due date
    - net
    - vat
    - gross
    - CIS
    - references (inv. #, order #, statement #, etc.)
    - isContinuation (page being processed is the same invoice, from a previous page, continued)
    - type (invoice, delivery note, statement, credit note, etc.)
    - isDuplicate
  - The data does not need to be human-readable at this point. The main concern at this point is speed, volume and usability from a computer's perspective.
- Dataframe
  - The data extracted should be processed thoroughly and the results should be saved in human-readable form under the appropriate headings.
  - A comment heading should have comments like confidence of the AI and anything the reviewer should know.
- Learning from the corrections.
  - Once the final result is made available to the user, the user should be able to make amendments and let the program know that the corrections have been made.
  - The AI should identify what has changed and update the paramaters accordingly. Next time, it should not make the same mistake.
  - This learning process can occur over a backend where it can learn from thousands of users' corrections. Allowing the program to become more effective at each use.
  - The learning process should account for the confidentiality of information.
- Processing the final data
  - Using the corrected data, the AI should prepare the final product.
  - Any mistake made here should again be ammendable so that the AI can learn from it too.
  - The processing should be consistent with the relevant framework.
- Review
  - After the user has reviewed the final product, the AI should prompt the user for how their experience was and what improvements would they like to see.
  - Paramaters should be set such that the AI tries to maximize user review.