 Program to consider the data given and find if there is any correlation between the heights and weights of the people in the data set
from csv import *

f= open("file-44.csv","r")
file=reader(f)
hgt=[]
wgt=[]
for row in file:
    hgt.append(row[1])
    wgt.append(row[2])
hgt=hgt[1:]
wgt=wgt[1:]
f.close()
'''
def bmi(h,w) :
    bmi=float(w)/float(h)**2
    return bmi

def calc_bmi(hgt,wgt):
    bmi_list=[]
    for i in range(len(hgt)):
        bmi_list.append(bmi((hgt[i]),(wgt[i])))
    return bmi_list

bmilist=calc_bmi(hgt,wgt)
avgbmi= sum(bmilist)/len(bmilist)
print(avgbmi)

bmi_dif=[]
for i in range(1,len(bmilist)):
    bmi_dif.append(abs(bmilist[i]-avgbmi))

#print(bmi_dif)
#print(sum(bmi_dif)/len(bmi_dif))

relationcounter=[]
for i in range(len(hgt)) :
    if abs(bmilist[i]-avgbmi)<0.01 :
        relationcounter.append(True)
    else :
        relationcounter.append(False)
# Finding the total number of true in the relationcounter list
print("True- ",relationcounter.count(True))
print("False- ",relationcounter.count(False))

'''
# Plotting height vs weight graph
import matplotlib.pyplot as plt
plt.scatter(hgt,wgt)
plt.show()
