# Adding SAVE Functionality to the Loan Qualifier Application

As part of best practices, we are adding new features and ehnahcements to the loan qualifier application.  

---

## Technologies

**Python 3.7** - *python version*

**Questionary** - *for interactive prompts*

**CSV** - *file save type*

**Fire** - *command line interface*

**Sys** - *system-specific parameters and functions*


---

## Installation Guide

Be sure to install required libraries

'''python
    install fire
    intall questionary
'''

---

## Usage

Use the new save functionality to save a list of qualifying loans:

'''python
    def save_qualifying_loans(qualifying_loans):
          wanna_save = questionary.text("Save the qualifying loans as a .csv (Y/N)?").ask()
          wanna_save = str(wanna_save)
          if wanna_save == "Y":
             import csv
             save_results = questionary.text("Enter file path to save as .csv").ask()
             save_results = Path(save_results)
             with open(save_results, 'w', newline='') as csvfile:
                 csvwriter = csv.writer(csvfile)
                  for row in qualifying_loans:
                     csvwriter.writerow(row)
'''



---

## Contributors

MBellD

---

## License

N/A
