# reverse_flatten_project

def flatten(y):

    for i in y:
        if isinstance(i,list):
            flatten(i)
        else:
            empty_list.append(i)

y= [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

empty_list = []
flatten(y)
print(empty_list)

def reverse(x):
    for i in range(int(len(x)/2)):
        temp = x[i]
        x[i]= x[len(x)-(i+1)]
        x[len(x)-(i+1)] = temp

    counter = 0
    for i in x:
        if isinstance(i,list):

            for a in range(int(len(i)/2)):
                temp = x[counter][a]
                x[counter][a] = x[counter][len(i)-(a+1)]
                x[counter][len(i)-(a+1)] = temp
                counter += 1
    print(x)

x = [[1, 2], [3, 4], [5, 6, 7]]
reverse(x)

[Patika.Dev](www.patika.dev)
