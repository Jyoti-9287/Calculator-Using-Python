# Calculator-Using-Python
from tkinter import *
from math import *
root=Tk()
root.geometry("450x600")
root.title("Calculator")
root.wm_iconbitmap('C:/Users/Dell/Downloads/c.ico')

svalue=StringVar()
svalue.set("")
screen=Entry(root,textvar=svalue, font="Arial 20 italic")
screen.pack(fill=X,ipadx=10,pady=10,padx=10)
f=Frame(root,bg="black")
f.pack()

def click(event):
    global svalue
    text=event.widget.cget("text")
    print(text)
    if text=='=':
        if svalue.get().isdigit():
            value=int(svalue.get())
        else:
            try:
                value=eval(screen.get())
            except Exception as e:
                print(e)
                svalue.set("Error")
                screen.update()

        svalue.set(value)
        screen.update()
    elif text=="C":
        svalue.set("")
        screen.update()
    elif text=="X":
        c=svalue.get()
        svalue.set(c[:len(c)-1])
        screen.update()
    else:
        svalue.set(svalue.get()+text)
        screen.update()

b0=Button(f,text='0', padx=5,pady=3,font='Arial 20 italic')
b0.pack(side=LEFT,ipadx=1,padx=5,pady=5)
b0.bind("<Button-1>",click)
b1=Button(f,text='1', padx=5,pady=3,font='Arial 20 italic')
b1.pack(side=LEFT,padx=5,pady=5)
b1.bind("<Button-1>",click)
b2=Button(f,text='2', padx=5,pady=3,font='Arial 20 italic')
b2.pack(side=LEFT,padx=5,pady=5)
b2.bind("<Button-1>",click)
b3=Button(f,text='3', padx=5,pady=3,font='Arial 20 italic')
b3.pack(side=LEFT,padx=5,pady=5)
b3.bind("<Button-1>",click)
b4=Button(f,text='4', padx=5,pady=3,font='Arial 20 italic')
b4.pack(side=LEFT,padx=7,pady=5)
b4.bind("<Button-1>",click)

f=Frame(root,bg="black")
f.pack()
b5=Button(f,text='5', padx=5,pady=3,font='Arial 20 italic')
b5.pack(side=LEFT,ipadx=2,padx=5,pady=5)
b5.bind("<Button-1>",click)
b6=Button(f,text='6', padx=5,pady=3,font='Arial 20 italic')
b6.pack(side=LEFT,padx=5,pady=5)
b6.bind("<Button-1>",click)
b7=Button(f,text='7', padx=5,pady=3,font='Arial 20 italic')
b7.pack(side=LEFT,padx=5,pady=5)
b7.bind("<Button-1>",click)
b8=Button(f,text='8', padx=5,pady=3,font='Arial 20 italic')
b8.pack(side=LEFT,ipadx=0,padx=5,pady=5)
b8.bind("<Button-1>",click)
b9=Button(f,text='9', padx=5,pady=3,font='Arial 20 italic')
b9.pack(side=LEFT,padx=6,pady=5)
b9.bind("<Button-1>",click)

f=Frame(root,bg="black")
f.pack()
b9=Button(f,text='.', padx=5,pady=3,font='Arial 20 italic')
b9.pack(side=LEFT,ipadx=7,padx=6,pady=5)
b9.bind("<Button-1>",click)
c0=Button(f,text='+', padx=5,pady=3,font='Arial 20 italic')
c0.pack(side=LEFT,padx=5,pady=5)
c0.bind("<Button-1>",click)
c1=Button(f,text='-', padx=5,pady=3,font='Arial 20 italic')
c1.pack(side=LEFT,ipadx=1,padx=5,pady=5)
c1.bind("<Button-1>",click)
c2=Button(f,text='*', padx=5,pady=3,font='Arial 20 italic')
c2.pack(side=LEFT,ipadx=3,padx=5,pady=5)
c2.bind("<Button-1>",click)
c3=Button(f,text='/', padx=5,pady=3,font='Arial 20 italic')
c3.pack(side=LEFT,ipadx=2,padx=5,pady=5)
c3.bind("<Button-1>",click)

f=Frame(root,bg="black")
f.pack()
c4=Button(f,text='%', padx=5,pady=3,font='Arial 18 italic')
c4.pack(side=LEFT,padx=6,pady=5)
c4.bind("<Button-1>",click)
d0=Button(f,text='**', padx=5,pady=3,font='Arial 18 italic')
d0.pack(side=LEFT,padx=5,pady=5)
d0.bind("<Button-1>",click)
d1=Button(f,text='.', padx=5,pady=3,font='Arial 18 italic')
d1.pack(side=LEFT,ipadx=5,padx=5,pady=5)
d1.bind("<Button-1>",click)
d2=Button(f,text='//', padx=5,pady=3,font='Arial 18 italic')
d2.pack(side=LEFT,padx=5,pady=5)
d2.bind("<Button-1>",click)
d3=Button(f,text='e', padx=5,pady=3,font='Arial 18 italic')
d3.pack(side=LEFT,ipadx=5,padx=5,pady=5)
d3.bind("<Button-1>",click)

f=Frame(root,bg="black")
f.pack()
d0=Button(f,text='(', padx=5,pady=3,font='Arial 18 italic')
d0.pack(side=LEFT,padx=5,pady=5)
d0.bind("<Button-1>",click)
d1=Button(f,text=')', padx=5,pady=3,font='Arial 18 italic')
d1.pack(side=LEFT,ipadx=5,padx=5,pady=5)
d1.bind("<Button-1>",click)
d2=Button(f,text='[', padx=5,pady=3,font='Arial 18 italic')
d2.pack(side=LEFT,padx=5,pady=5)
d2.bind("<Button-1>",click)
d3=Button(f,text=']', padx=5,pady=3,font='Arial 18 italic')
d3.pack(side=LEFT,padx=5,pady=5)
d3.bind("<Button-1>",click)
d3=Button(f,text='{', padx=5,pady=3,font='Arial 18 italic')
d3.pack(side=LEFT,padx=5,pady=5)
d3.bind("<Button-1>",click)
d3=Button(f,text='}', padx=5,pady=3,font='Arial 18 italic')
d3.pack(side=LEFT,padx=5,pady=5)
d3.bind("<Button-1>",click)

f=Frame(root,bg="black")
f.pack()
d2=Button(f,text='sin', padx=5,pady=3,font='Arial 18 italic')
d2.pack(side=LEFT,padx=6,pady=5)
d2.bind("<Button-1>",click)
d3=Button(f,text='cos', padx=5,pady=3,font='Arial 18 italic')
d3.pack(side=LEFT,padx=6,pady=5)
d3.bind("<Button-1>",click)
d3=Button(f,text='tan', padx=5,pady=3,font='Arial 18 italic')
d3.pack(side=LEFT,padx=6,pady=5)
d3.bind("<Button-1>",click)
d0=Button(f,text='C', padx=5,pady=3,font='Arial 18 italic')
d0.pack(side=LEFT,ipadx=5,padx=5,pady=5)
d0.bind("<Button-1>",click)

f=Frame(root,bg="black")
f.pack()
d0=Button(f,text='log10', padx=5,pady=3,font='Arial 18 italic')
d0.pack(side=LEFT,padx=5,pady=5)
d0.bind("<Button-1>",click) 
d1=Button(f,text='sqrt', padx=5,pady=3,font='Arial 18 italic')
d1.pack(side=LEFT,padx=5,pady=5)
d1.bind("<Button-1>",click)
d0=Button(f,text='X', padx=5,pady=3,font='Arial 18 italic')
d0.pack(side=LEFT,padx=5,pady=5)
d0.bind("<Button-1>",click)
d0=Button(f,text='=', padx=5,pady=3,font='Arial 18 italic')
d0.pack(side=LEFT,ipadx=3,padx=5,pady=5)
d0.bind("<Button-1>",click)

root.mainloop()
