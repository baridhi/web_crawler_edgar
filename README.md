# Welcome to the SEC.gov EDGAR Crawler!  
---

### Background  

* This crawler parses fund holdings from Edgar, which are reported 
in quarterly-filed 13F documents.  

* 13F documents are filed by Private Trusts, Banks, Insurance
Companies, Investment Advisors, Institutional Managers and
Hedge Funds, but _**not**_ Mutual Funds.

* *To retrieve fund holdings you must enter a valid CIK;*
not all CIKs return 13Fs.  

* To procure the CIK of a mutual fund you will need to 
ascertain the name of the institutional manager for that 
mutual fund.  

* For example, Sequoia Fund is a mutual fund, but they do not file 
a 13F. However, Sequoia's institutional manager, "Ruane, Cunniff & 
Goldfarb Inc", does file a 13F. Therefore, by using Ruane Cunniff's 
CIK you can successfully locate the 13F that reflects Sequoia's holdings.  

* If you need help searching for valid CIKs this website helps:  
https://www.sec.gov/edgar/searchedgar/cik.htm  
Then review the filings to make sure that the fund files 13Fs.  

* Here are some valid CIKs to test:  

| Fund                      | CIK        |
| ------------------------  | ---------- |
| BlackRock Fund Advisors   | 0001006249 |
| Bridgewater Associates    | 0001350694 |
| Renaissance Technologies  | 0001037389 |
| Ruane, Cunniff & Goldfarb | 0000728014 |

---

### Installation  
1. Download the .zip file that was emailed to you. Email me at 
shauncox44@gmail.com if you need the file.  
2. Open the .zip file.  
3. Make sure that you have the `scrapy`, `minidom` and `urllib.request`
Python libraries installed.  

---

### Instructions  
1. Open your terminal.  
2. Navigate to the crawler directory :  
`$ cd shaun_cox_edgar_crawler/edgar`  
3. Run the scraper:  
`$ scrapy crawl edgar_search -a cik=xxxxxxxxxx`  
  a. xxxxxxxxxx will be the valid CIK that you've chosen  
4. Wait about 5 seconds for the crawler to run.  
5. The output file will save in the `shaun_cox_edgar_crawler/edgar` directory.  
  a. Example output file: `0001350694.txt`  
6. Now, you can open the .txt file with Excel or the Python CSV module and 
view all of the holdings including shares and value per holding.  

---

### Support  
If you have issues running the crawler please email Shaun at 
shauncox44@gmail.com  