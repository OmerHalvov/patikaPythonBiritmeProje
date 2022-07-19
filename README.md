# patikaPythonBiritmeProje
Patika Python Bitirme Projesi

1- l[0] = [1,'a',['cat'],2] -------->list tipinde ise liste tekrar flatten fonsiyonunu çağır.
          -l=1
          -l='a'
          -l=['cat']        -------->list tipinde ise liste tekrar flatten fonsiyonunu çağır.
              - l='cat'
          -l=2
        
2- l[1] = [[[3]],'dog']    -------->list tipinde ise liste tekrar flatten fonsiyonunu çağır.
          -l=[[3]]         -------->list tipinde ise liste tekrar flatten fonsiyonunu çağır.
              -l=[3]       -------->list tipinde ise liste tekrar flatten fonsiyonunu çağır.
                 -l=3
          -l='dog'
3- l[2] = 4
4- l[3] = 5
"""

l = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]
lnew = []
def flatten(n):
    for i in n:
        if isinstance(i, list):
            flatten(i)
        else:
            lnew.append(i)

flatten(l)
print(lnew)

l =[[1, 2], [3, 4], [5, 6, 7]]
l=l[::-1]

for i in range(len(l)):
    (l[i])=(l[i])[::-1]
print(l)
