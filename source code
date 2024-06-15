SOURCECODE:
BackEnd:
$ mysql -u USERNAME -p
ENTER PASSWORD:PASSWORD
mysql&gt; use DATABASENAME;
mysql&gt; create table student (sname char(100),rollno varchar(20),gender char(20),year int,Branch
char(20));
mysql&gt;exit
FrontEnd:
import tkinter as t
import mysql.connector
def f1():
x = v1.get()
y = v2.get()
p = v3.get()
q = v4.get()
r = v5.get()
d = mysql.connector.connect(host = &quot;Localhost&quot;, user = &quot;USERNAME&quot;, password =
&quot;PASSWORD&quot;, database = &quot;DATABASENAME&quot;)
c = d.cursor()
z = &quot;insert into student(sname,rollno,gender,year,branch)values(%s,%s,%s,%s,%s)&quot;
a = (x,y,p,int(q),r)
c.execute(z,a)
d.commit()
d.close()
w = t.Tk()
w.title(&quot;Student Registration Form&quot;)
l1 = t.Label(text = &quot;Name&quot;)
l1.place(x = 100, y =50)
v1 = t.StringVar()
t1 = t.Entry(text = &quot; &quot;, textvariable = v1)
t1.place(x = 200, y = 50)
l2 = t.Label(text = &quot;Roll No.&quot;)
l2.place(x = 100, y = 100)
v2 = t.StringVar()
t2 = t.Entry(text = &quot; &quot;, textvariable = v2)
t2.place(x = 200, y = 100)
v3 = t.StringVar()
l3 = t.Label(text = &quot;Gender&quot;)
l3.place(x = 100, y = 150)
r1 = t.Radiobutton(w, text = &quot;male&quot;, variable = v3, value = &quot;male&quot;, command = f1)
r1.pack()
r1.place(x = 100, y =150)
r2 = t.Radiobutton(w, text = &quot;female&quot;, variable = v3, value = &quot;female&quot;, command = f1)
r2.pack()
r2.place(x = 200, y = 150)
l4 = t.Label(text = &quot;year&quot;)
l4.place(x = 100, y = 200)
v4 = t.IntVar()
v4.set(&quot;Select your year&quot;)
drop = t.OptionMenu(w,v4,&quot;1&quot;,&quot;2&quot;,&quot;3&quot;,&quot;4&quot;)
drop.pack()
drop.place(x = 200, y = 250)
l5 = t.Label(w , text= &quot;Branch&quot;)
l5.place(x = 100, y = 300)
v5 = t.StringVar()
v5.set(&quot;Select your Branch&quot;)
drop = t.OptionMenu(w, v5, &quot;CSE&quot;,&quot;AIML&quot;,&quot;DS&quot;,&quot;ECE&quot;)
drop.pack
drop.place(x = 200, y = 300)
b = t.Button(text = &quot;Submit&quot;, command = f1)
b.place(x = 300, y = 400)
w.mainloop()
