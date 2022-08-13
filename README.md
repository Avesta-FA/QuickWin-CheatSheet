# QuickWin-CheatSheet
The purpose of this repository is to be a cheat sheet for the security community to find and detect adversaries.  
While there will be a lot of quick wins I will also add detection techniques that require more analysis.  

## General

### Long tail analysis
Long tail analysis is a multi purpose detection technique that works on historical data. The output contains two important sections:  
* Least frequently used (LFU)  
* Most frequently used (MFU)  

Depending on the data that is being analyzed both sections can be interesting.  
This technique was originally founded by Eric Conrad, SANS Instructor.  
https://www.youtube.com/watch?v=KgVmNicfHxo

#### How To  

` Data | Group-Object id -NoElement | sort count`  
` Data | sort | uniq -c | sort -n`  



