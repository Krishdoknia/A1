# A1
#COMPOUNDED INTEREST
from datetime import date

s_d=int(input("Start date :"))
s_m=int(input("Start month :"))
s_y=int(input("Start year :"))

e_d=int(input("End date :"))
e_m=int(input("End month :"))
e_y=int(input("End year :"))

p=float(input("Principal =Rs."))
i_r=float(input("Interest rate(in % per annum) ="))

#r= rate_per_100*12

print("\t",e_d,"/",e_m,"/",e_y,"\n","\t",s_d,"/",s_m,"/",s_y)

from datetime import date

s_date= date(s_y, s_m, s_d)
e_date= date(e_y, e_m, e_d)

rz= e_date-s_date

num_days=rz.days

print(num_days)

if num_days>=365:
  Years=num_days//365
  print(Years)
  rem_d1=num_days%365
  print(rem_d1)
  if rem_d1>=30:
    Months=rem_d1//30
    print(Months)
    rem_d2=rem_d1%30
    print(rem_d2)
    print(Years,"Y ",Months,"M ",rem_d2,"D")
    
    m=Months+float(rem_d1/30)
    y=Years+float(m/12)
    c_i=float((p*(((100+i_r)/100)**float(y)))-p)
    
    print("Compound interest =Rs.",c_i)
    print("Total amount =Rs.",c_i+p)

  else :
    print(rem_d1) 
    print(Years,"Y ",rem_d1,"D") 
    
    y1=Years+float(rem_d1/365)
    c_i1=float((p*(((100+i_r)/100)**y1))-p)
    print("Compound interest =Rs.",c_i1)
    print("Total amount =Rs.",c_i1+p)


elif num_days>=30 and num_days<365:
  Months1=num_days//30
  print(Months1)
  rem_d3=num_days%30
  print(rem_d3)
  print(Months1,"M ",rem_d3,"D")
  
  m1=Months1+float(rem_d3/30)
  y2=float(m1/12)
  c_i2=float((p*(((100+i_r)/100)**float(y2)))-p)
  print("Compound interest =Rs.",c_i2)
  print("Total amount =Rs.",c_i2+p)
  
else :
  print(num_days)
  print(num_days,"D")

  y3=float(num_days/365)
  c_i3=float((p*(((100+i_r)/100)**float(y3)))-p)

  print("Compound interest =Rs.",c_i3)
  print("Total amount =Rs.",c_i3+p)
