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

------------------------------
*+形参：把所有实参以元组的形式赋值于形参
**+形参：加倍

------------------------------
with open("fruits.txt") as myfile:
    content=myfile.read()
读取并关闭文件（关闭操作被隐藏）

with open("files/vegetables.txt","w") as myfile:
    myfile.write("ocucumber\nonion\ncarrot")
写入操作

with open("files/flavor.txt","x") as myfile:
    myfile.write("okra")
创建新file并写入数据

with open("files/fruits.txt","a") as myfile:
    myfile.write("okra")
不删除原有文件并在已有的文件末尾写入

myfile.seek(20)：指针

Python 中打开一个文件的函数 open() 的第二个参数指明了打开的模式. 可以赋予该参数的实参 *枚举* 如下 : 
'r', 'r+', 'w', 'w+', 'a', 'a+', 'rU'

其中 : 
'r' : 以只读模式打开
'r+' : 以读写模式打开, 写的指针刚开始指在文件开头, 因此会覆写文件
'w' : 清空文件, 不能使用 <file>.read*() 方法.  (read(), readline(), readlines())
'w+' : 清空文件, 可以使用 <file>.read*() 方法. 
'a' : 向一个文件追加内容,  不能使用 .read*()
'a+' : 向一个文件追加内容, 可以使用 .read*()
'rU' : 自动探测行尾符, 如果以这种模式打开一个文件, 该文件对象将获得一个 newlines 属性, 当还未读到任何行尾时, <file>.newlines 属性等于 None, 读到了则可能是'\n', '\r\n', '\r' 中的一种
    
    --------------------------
    import time

str=''

with open("files/fruits.txt") as myfile:
    content= myfile.read()
    str= content.replace('\n','')
    print(str)



with open("files/fruits.txt","w") as myfile:
    myfile.write(str)
    
--------------------------
docs.python.data=json.load(open("data.json"))

-------------------------
fetchall() ：
   返回多个元组，即返回多条记录(rows),如果没有结果,则返回 ()
