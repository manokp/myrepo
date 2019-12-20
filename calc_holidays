#!/usr/bin/env python
from datetime import timedelta, date
import datetime, calendar 

 
def daterange(date1, date2):
    #cnt is the difference between two dates
    global cnt
    cnt = ((date2 - date1).days) +1
    print("cnt", cnt)
   # with open("../holidays_list.txt") as file_holidays:
	 #	    holidays = file_holidays.readlines()
    holidays = ["2019-11-01","2020-01-01","2019-12-25","2019-12-31"]
    for noof_days in range(cnt):
        wk_date = date1 + timedelta(noof_days)
        wk_date1 = calendar.day_name[wk_date.weekday()]
        str_startdate = str(wk_date)
      #holiday check
        for i in holidays:
            if str_startdate in i:
                cnt = cnt-1
            else:
                continue
      #weekend check
        if wk_date1 in {'Sunday', 'Saturday'}:
            cnt= cnt -1 
    #for_loop_ends
    return(cnt)
######
start_dt1 = "2019-12-24"
end_dt1 = "2020-01-02"
start_dt = datetime.datetime.strptime(start_dt1, "%Y-%m-%d").date()
end_dt = datetime.datetime.strptime(end_dt1, "%Y-%m-%d").date()
daterange(start_dt, end_dt)
print(cnt)
