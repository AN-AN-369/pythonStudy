# pythonStudy
-tuple：(1,4,5)
-list[1,4,5]
-dictionary:{1,4,5} 自动排序且不能出现相同元素

-------------------------------------
name=input("Enter your name:")
surname=input("Enter your surname:")
when="today"
message="Hello %s %s" % (name,surname)
message=f"Hello {name} {surname} .What's up {when}"

outcome：Enter your name:dada
Enter your surname:dada
Hello dada dada What's up today

--------------------------
monday_temperatures=[9.1,8.8,7.6]
print(round(monday_temperatures[0]))              备注：round函数为四舍五入

：9
for循环：for temperature in monday_temperatures:

for letter in 'hello':
    print(letter）
h
e
l
l
o
    print(letter.title())：中加title为大写字母
H
E
L
L
O

-------------------------------
item(): ('Marry',9.1)
keys(): Marry
values(): 9.1

-------------------------------
interrogatives=("how","what","why")
.startswith(interrogatives)
解释：检验是否存在和元组中相同的元素

-------------------------------
"{}"format():按照顺序输出
append():在列表末尾添加新的对象

------------------------------

def sentence_maker(phrase):
    interrogatives=("how","what","why")
    capitalized=phrase.capitalize()
    if phrase.startswith(interrogatives):
        return "{}?".format(capitalized)
    else:
        return "{}.".format(capitalized)

results=[]
while True:
    user_input=input("Say somehthing:")
    if user_input=="\end":
        break
    else:
        results.append(sentence_maker(user_input))

print(" ".join(results))

-------------------------------
"".join(result)

------------------------------
temps=[221,234,340,314]
new_temps=[temp/10 if temp!=314 else 1 for temp in temps]
print(new_temps)
