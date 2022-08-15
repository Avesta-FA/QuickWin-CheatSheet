# QuickWin-CheatSheet
The purpose of this repository is to be a cheat sheet for the security community to find and detect adversaries.  
While there will be a lot of quick wins I will also add detection techniques that require more analysis.  


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

### Stacking
Generally, endpoints tend to be very similar especially if you have a baseline configuration.  
When you gather data from your endpoints  (e.g Registry) you can perform what is called stacking.  
When you stack the specified data from all the endpoints you will end up with entries that only exist on a small number of endpoints. Those entries are the ones you want to analyze.  
  
A great tool that utilizes this technique is called [Kansa](https://github.com/davehull/Kansa/) by dave hull.  


