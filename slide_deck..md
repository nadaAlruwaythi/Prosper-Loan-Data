##  Prosper Loan Data Exploration
 
##### By Nada Alruwaythi

##### Investigation Overview
* In this investigation, I wanted to figure out two things:

- 1- The variables that can be utilized to forecast credit default.
- 2- What variables determine Prosper's rating.

Dataset Overview
This data set contains 113937 loans with 81 variables on each loan, for the purpose of this investigation I've taken the following variables: 
 - Term
 - LoanStatus
 - BorrowerRate
 - ProsperRating (Alpha)
 - LoanOriginalAmount
 - ProsperRating (numeric)
 - EmploymentStatus
 - DelinquenciesLast7Years
 - StatedMonthlyIncome
 - Recommendations
 - Investors
 - TotalProsperLoans

## Wrangling


# Univariate Exploration

### Loan status


- The majority of the loans in the data set are current loans. Past-due loans are classified into numerous categories based on the length of the payment delay.
- Another significant factor is completed loans, with defaulted loans constituting a minority.


    
![png](slide_deck._files/slide_deck._9_0.png)
    


# Bivariate Exploration

- There is insufficient information on part-time, retired, and unemployed borrowers for the job status variable to demonstrate how it interacts with term and Prosper rating factors. However, it is clear that word and Prosper rating interact in some way. There are proportionally more 60-month loans with B and C grades. Borrowers with HR ratings can only get loans for 36 months.


    
![png](slide_deck._files/slide_deck._12_0.png)
    


- The most frequent rating among defaulted loans is actually D and E.
- And the most frequent rating among Completed is alsoDand second highest is E and so on




    <AxesSubplot:xlabel='LoanStatus', ylabel='count'>




    
![png](slide_deck._files/slide_deck._14_1.png)
    


# Multivariate Exploration




    Current      56576
    Completed    38074
    Defaulted    17010
    Name: LoanStatus, dtype: int64



- Business and home improvement don't have nearly equivalent means at all, with the exception of auto.
- Business-related categories typically have more


    
![png](slide_deck._files/slide_deck._18_0.png)
    


- Except for the lowest ratings defaulted credits tend to be larger than completed.
- Most of the defaulted credits comes from individuals with low Prosper rating


    
![png](slide_deck._files/slide_deck._20_0.png)
    


    C:\Users\nadaa\anaconda3\anaconda\lib\site-packages\traitlets\traitlets.py:2556: FutureWarning: --TagRemovePreprocessor.remove_cell_tags={"skip"} for containers is deprecated in traitlets 5.0. You can pass `--TagRemovePreprocessor.remove_cell_tags item` ... multiple times to add items to a list.
      warn(
    [NbConvertApp] Converting notebook slide_deck..ipynb to markdown
    [NbConvertApp] Support files will be in slide_deck._files\
    [NbConvertApp] Making directory slide_deck._files
    [NbConvertApp] Making directory slide_deck._files
    [NbConvertApp] Making directory slide_deck._files
    [NbConvertApp] Making directory slide_deck._files
    [NbConvertApp] Writing 2803 bytes to slide_deck..md
    

    [NbConvertApp] Converting notebook slide_deck..ipynb to slides
    [NbConvertApp] Writing 787533 bytes to slide_deck..slides.html
    [NbConvertApp] Redirecting reveal.js requests to https://cdnjs.cloudflare.com/ajax/libs/reveal.js/3.5.0
    Traceback (most recent call last):
      File "C:\Users\nadaa\anaconda3\anaconda\Scripts\jupyter-nbconvert-script.py", line 10, in <module>
        sys.exit(main())
      File "C:\Users\nadaa\anaconda3\anaconda\lib\site-packages\jupyter_core\application.py", line 270, in launch_instance
        return super(JupyterApp, cls).launch_instance(argv=argv, **kwargs)
      File "C:\Users\nadaa\anaconda3\anaconda\lib\site-packages\traitlets\config\application.py", line 845, in launch_instance
        app.start()
      File "C:\Users\nadaa\anaconda3\anaconda\lib\site-packages\nbconvert\nbconvertapp.py", line 350, in start
        self.convert_notebooks()
      File "C:\Users\nadaa\anaconda3\anaconda\lib\site-packages\nbconvert\nbconvertapp.py", line 524, in convert_notebooks
        self.convert_single_notebook(notebook_filename)
      File "C:\Users\nadaa\anaconda3\anaconda\lib\site-packages\nbconvert\nbconvertapp.py", line 491, in convert_single_notebook
        self.postprocess_single_notebook(write_results)
      File "C:\Users\nadaa\anaconda3\anaconda\lib\site-packages\nbconvert\nbconvertapp.py", line 463, in postprocess_single_notebook
        self.postprocessor(write_results)
      File "C:\Users\nadaa\anaconda3\anaconda\lib\site-packages\nbconvert\postprocessors\base.py", line 28, in __call__
        self.postprocess(input)
      File "C:\Users\nadaa\anaconda3\anaconda\lib\site-packages\nbconvert\postprocessors\serve.py", line 90, in postprocess
        http_server.listen(self.port, address=self.ip)
      File "C:\Users\nadaa\anaconda3\anaconda\lib\site-packages\tornado\tcpserver.py", line 151, in listen
        sockets = bind_sockets(port, address=address)
      File "C:\Users\nadaa\anaconda3\anaconda\lib\site-packages\tornado\netutil.py", line 161, in bind_sockets
        sock.bind(sockaddr)
    OSError: [WinError 10013] An attempt was made to access a socket in a way forbidden by its access permissions
    
