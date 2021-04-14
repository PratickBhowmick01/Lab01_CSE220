# Lab01_CSE220
Lab assignments

#Task05 #Splits an array as a balanced beam
#Lab-1
A = []            #Taking array input 
i = 0
while (i < 5):
    num = int(input("Please enter the integer: "))
    A.append(num)
    i += 1

def splitArray(a):
    result = True
    l_pan, r_pan = a[0], a[-1] 
    count = len(a) - 2
    i = 1              
    j = len(a)-2        
    
    while(count > 0):          
        if (l_pan < r_pan):
            l_pan += a[i]
            j += 1
        else:
            r_pan += a[j] 
            i -= 1
            
        # print(l_pan, r_pan)
        i += 1
        j -= 1
        count -= 1
        
    if (l_pan != r_pan):
        result = False
    return result
    
print(splitArray(A)) 

