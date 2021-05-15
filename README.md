# TestAutomation

![Alt Text](https://github.com/christianshub/TestAutomation/blob/main/Snapshots/demo.gif)

## What is this?
This is an automation tool that reads excel files to help non-IT people in creating easy automated tests. 

The tool can also be used if someone needs an automated task done quick without the need to write any code. 

## How do I install and run it?
1) Compile TestAutomation
2) Download the latest chrome driver here: https://chromedriver.chromium.org/downloads, and insert the driver (`chromedriver.exe`) into the same directory from where `TestAutomation.exe` is located
3) Create excel files containing your test cases in the same directory from where `TestAutomation.exe` is located
    - 3.1) The first excel file you want to open should specificy the webpage you want to visit.
    - 3.2) Note, the tool iterates over all excel files and sorts them by the lowest numerical value first. From the files below, we would first read `00_Open.xlsx`, then `01_SignUp.xlsx` and so forth:
        - 00_Open.xlsx
        - 01_SignUp.xlsx
        - 02_SignInPage.xlsx    
4) Run `TestAutomation.exe`

## How do I write a Test Case


### Details 


5 columns needs to be filled for each step in your test case. Each column is described below followed by examples:

- `XPATH`: Find the element you want to interact with in your browser.
    - To retrieve the xpath: Right click on the element in your browser -> choose inspect -> in DevTools -> Right click -> Copy -> Copy full xpath
- `Action`: Consists of three comands; `open`, `click`, `send`
    - `open`: Opens a webpage
    - `click`: Clicks on an element (e.g. a button) found by the xpath
    - `send`: Sends some input (e.g. username field) found by the xpath 
- `Input`: Username, e-mails etc. should be inserted here
- `Step text`: Insert a descriptive text of your current step (used for logging)
- `WindowTitle`: Insert the window title of the webpage you visit (needed if navigation between different pages/pop-up windows)   

NB: Make sure the cells in the excel files are text formatted. Also, empty fields should be marked with `- `

### Examples

| XPATH      	| Action 	| Input 	| Step text                   	| WindowTitle                             	|
|------------	|--------	|-------	|-----------------------------	|-----------------------------------------	|
| /html/body 	| Click  	| -     	| Clicks the 'Sign up' button 	| GitHub: Where the world builds software 	|



## To-do

- Sheet navigation possibility.
- Seperate into sub methods for readability.
- Use logfiles to write an error report with reproduceable steps.
