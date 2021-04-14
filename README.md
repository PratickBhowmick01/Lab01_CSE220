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

#Task09: Palindrome

array = [10,20,0,0,0,10,20,30]   #size=5, size = 5, length = 8
def palindrome(a,start,size): 
    temp = []
    i = (start+size-1) % len(a)   #last index
    count = 0
    while(count < size):        #storing in reverse pattern
        temp.append(a[i])
        count += 1
        i -= 1
        if(i < 0):
            i = len(a) - 1    
            
    result = "True"         #checking for palindrome
    count = 0
    ind = start
    while(count < size):
        if(temp[count] != a[ind]):
            result = "False"
            break         
        count += 1
        ind = (ind + 1) % len(a)
    
    if(result == "True"):
        return True 
    else:
        return False
                
print(palindrome(array,5,5)) 










