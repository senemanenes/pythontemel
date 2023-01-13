# pythontemel

#Ödev 1

lst=[4,6,1,2,["a",2,11],"cat","B",[2,[4,8]]]

lst_flatten = []
def flatten(l):
    for sublist in l:    #listenin içinde liste olan bir eleman var mı?
        if isinstance(sublist, list):
            flatten(sublist)

        else:    
          
            lst_flatten.append(sublist)  #listenin içinde liste olmayan elemanları boş olan listeye ekle
    
    return lst_flatten

print(flatten(lst))


#Ödev 2

l2=[[1, 2], [3, 4], [5, 6, 7],[[9,10],[11,12]]]

l2_flat=[]

def flat2(l):
    l.reverse()
    for sublist in l:
        if isinstance(sublist,list):
            flat2(sublist)

        else:
            l2_flat.append(sublist)
    
    return l2_flat
print(flat2(l2))
