# project-metro-
#bach tchof lwijha ta3k o ch7ale tiki
# now project metro name de station and achti tikite
import tkinter
from tkinter import ttk
from tkinter import messagebox
from tkinter import *

met = tkinter.Tk()
met.title('metro de alge :)')  # title de forme
met.geometry('800x500')  # size the forme
met.config(background='light green')  # color de bg
###################################################################
# hna ndir tof
canvas = Canvas(met,width = 600, height = 150) # hajm canvas
canvas.pack() # ybyli canvas
img = PhotoImage(file = 'python-logo.png') # hna tof asmha
canvas.create_image(0,0,image=img,anchor=NW) # hna mnin ybda rasm photo 
####################################################################
# bach n3rfe cha5se male or fimale or mou5anet
v = StringVar()
v.set('male')
rdom = Radiobutton(met,text = 'Male',value = 'male',variable = v,bg = 'light green')
rdom.pack()

rdof = Radiobutton(met,text = 'Fimale',value = 'fimale',variable = v,bg = 'light green')
rdof.pack()

rdon = Radiobutton(met,text = 'Effeminate',value = 'effeminate',variable = v,bg = 'light green')
rdon.pack()
def f():
    print(v.get())
Button(met,text = 'enter yor sex',font = 'impact 15',background = 'blue',foreground = 'black',command =f).pack()
#####################################################################
# ther code ndir lforma flwste
w = 600
h = 400
sw = met.winfo_screenwidth()
sh = met.winfo_screenheight()
x = (sw - w) / 2
y = (sh - h) / 2
met.geometry('%dx%d+%d+%d' % (w, h, x, y))
#######################################################################
# nkteb text welcom to metro DALG
lbe = ttk.Label(met, text='* WELCOM TO METRO ALGERIA : مرحبا بكم في مترو الجزائر *', background='light green',
                font='tahoma 25')  # text to metro
lbe.pack()
#########################################################################
#button por clic
fnt = ('tahoma', 22) # nw3e l5et o lhjm ta3o
botns = ttk.Style() # style li yjo fih ga3 li bouton
botns.configure('TButton',font=fnt, background='red',foreground = 'blue') # color ta3 bg o fg o hjme lboton
#botn = ttk.Button(met, text='ok') # lbutton bhde dato
#botn.pack() # hna std3it lboton
#########################################################################

##########################################################################
#9aimate sondo9e
lbx = Listbox(met,fg = 'red',bg = 'black',font = 'tahoma 15')
lbx.insert(0,'oussama')
lbx.insert(1,'kamale')
lbx.insert(2,'fathi')
lbx.insert(3,'so3ade')
lbx.insert(4,'raniya')
lbx.insert(5,'nihale')
lbx.insert(6,'sami')
lbx.insert(7,'noura')
lbx.pack()

def lis():
    print(lbx.get(ACTIVE))
Button(met,text = 'enter yor name ',font = 'tahoma 16',command = lis).pack()
############################################################################
# lalist ta3i o fiha ga3 li station

lis = ttk.Combobox(met, font = 'tahoma 16', values = ('liste de metro alg - hai el badr','place des martyrs','ali boumendjel','tafourah grande poste','khelifa boukhalfa','1er mai','aissat idir','hamma','jardin dessais','les fusilles','cite amiroche','cite mer & soleil','hai el badr','liste de metro hai el badr - el harrach centre','bachdjerh tennis','bachdjarah','el harrach gare','el harrach centre','liste de metro hai el badr - ain naadja','les ateliers','gue de constantine','ain nadja'),state = 'readonly')
lis.current(0) # lasm ta3 lmhata li y5roj lwle f lalist hna rani dert lwale
lis.pack() # hna bach ytb3holi
##############################################################################################################################################
v = BooleanVar() #bach nchof wch y5rjli true or false or int or string
cx = Checkbutton(met,text = ' enter yor trou',bg = 'light green',font = 'tahoma 15',variable = v) # hna bach ychkli lmourab3
cx.pack() # hna bach ytb3o

def s(): # hdi dala ta3 lboutouna
    print(v.get()) # hdi bach ytba3li true or foalse
Button(met,text = 'ok',bg = 'red',font = 'tahoma 16',command = s).pack() #hdi lboutton bach ki n3bze 3liha ida konte m3alm 3la lmourab3 yirli true ida nn ydirli foalse
###################################################################################################################
def ntealg(): # dala li ji fiha messagebox
    messagebox.showinfo('welom to metro alg ','yor destinasyon is  50 DA ticit: '+lis.get()) # mesage box li y5roj llmouste5dm

metn = ttk.Button(met,text = 'clic here',command = ntealg) # hna lboutton bach ki nclici 3lih y5rjli lamer
metn.pack() # whna std3itha bach t5rjli ntija
#############################################################################


met.mainloop() # fien de programe
