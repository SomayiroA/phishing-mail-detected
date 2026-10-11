# Phishing Email 📧

This phishing email was marked with a high severity so i had to thoroughly analyse the details and c2 addresses to ascertain it it was a true positive or not.

## Alert Summary and Timeline. ⌛

A phishing email was detected on 2021-06-13. It contained a zipped Excel File that was sent from trenton@tritowncomputers.com to lars@letsdefend.io. 

## Investigation steps. ✅

I ran a sandbox analysis of the attached Excel file and obtained c2 addresses. when i searched the c2 addresses on Log Management, i saw that the malicious excel file had beem ran by Lars. to furher confirm, i looked for the Lars source address on Endpoint Management and clarified that the LarsPRD device communicated with the malicious address.

##My Findings, Conclusion, and Recommended Response. 🙋‍♀️

I also examined the LarsPRD CMD history and saw that the regsvr32 commannd that is included in Excel 4.o macros has been run. 
I flagged the alert as a true positive and escalated it to SOC 2 Analyst for further action.

## Screenshots 📷

<img width="410" height="236" alt="Screenshot 2026-10-10 124512" src="https://github.com/user-attachments/assets/d1d361de-61fa-4171-8839-4f2044395a8d" />
<img width="393" height="92" alt="Screenshot 2026-10-10 124521" src="https://github.com/user-attachments/assets/5940a845-16fb-4a3f-b49b-a83f7b5403c4" />

## Lessons Learned 🌿

i learnt how to search for c2 addresses and comfirm from the receiver's end if a URL or attachment has been opened and if it has been executed by the sender.
