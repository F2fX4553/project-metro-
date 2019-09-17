# project-metro-
#bach tchof lwijha ta3k o ch7ale tiki
# now project metro name de station and achti tikite
import tkinter
from tkinter import ttk
from tkinter import messagebox

met = tkinter.Tk()
met.title('metro de alge :)')  # title de forme
met.geometry('600x400')  # size the forme
met.config(background='light green')  # color de bg
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
# button por clic
fnt = ('tahoma', 22) # nw3e l5et o lhjm ta3o
botns = ttk.Style() # style li yjo fih ga3 li bouton
botns.configure('TButton',font=fnt, background='red',foreground = 'blue') # color ta3 bg o fg o hjme lboton
botn = ttk.Button(met, text='ok') # lbutton bhde dato
botn.pack() # hna std3it lboton
#########################################################################
# lalist ta3i o fiha ga3 li station
lis = ttk.Combobox(met, font = 'tahoma 16', values = ('liste de metro alg - hai el badr','place des martyrs','ali boumendjel','tafourah grande poste','khelifa boukhalfa','1er mai','aissat idir','hamma','jardin dessais','les fusilles','cite amiroche','cite mer & soleil','hai el badr','liste de metro hai el badr - el harrach centre','bachdjerh tennis','bachdjarah','el harrach gare','el harrach centre','liste de metro hai el badr - ain naadja','les ateliers','gue de constantine','ain nadja'),state = 'readonly')
lis.current(0) # lasm ta3 lmhata li y5roj lwle f lalist hna rani dert lwale
lis.pack() # hna bach ytb3holi
def ntealg(): # dala li ji fiha messagebox
    messagebox.showinfo('welom to metro alg ','yor destinasyon is  50 DA ticit: '+lis.get()) # mesage box li y5roj llmouste5dm
metn = ttk.Button(met,text = 'clic here',command = ntealg) # hna lboutton bach ki nclici 3lih y5rjli lamer 
metn.pack() # whna std3itha bach t5rjli ntija 

met.mainloop() # fien de programe 

