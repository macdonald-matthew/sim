import streamlit as st
import random

def SHOT_SIM(A_Shooter1,S_Shooter1,
             A_Shooter2,S_Shooter2,
             A_Shooter3,S_Shooter3,
             A_Shooter4,S_Shooter4,
             A_Shooter5,S_Shooter5,
             A_Shooter6,S_Shooter6,
             A_Shooter7,S_Shooter7,
             A_Shooter8,S_Shooter8,
             A_Shooter9,S_Shooter9,
             A_Shooter10,S_Shooter10,
             N_Shields,S_Shields,Defense):
    winner=0  #No winner to start
    num_b_mis1=S_Shooter1
    num_b_mis2=S_Shooter2
    num_b_mis3=S_Shooter3
    num_b_mis4=S_Shooter4
    num_b_mis5=S_Shooter5
    num_b_mis6=S_Shooter6
    num_b_mis7=S_Shooter7
    num_b_mis8=S_Shooter8
    num_b_mis9=S_Shooter9
    num_b_mis10=S_Shooter10
    shields=N_Shields
    while winner==0: #keep going to Red or Blue wins
        if num_b_mis1>0:
            B_shoot1=random.randint(1, A_Shooter1)  #every GBASM fires or all remaining missiles fired if less than surviving GBASMs
            num_b_mis1-=1  #number of missiles decreases by number fired
            if B_shoot1>=S_Shields:  #if any of the missiles hit, B wins
                shields-=1
            if shields<0:  #if B runs out of missiles, R wins
                if B_shoot1>=Defense:  #if B runs out of missiles, R wins
                    winner+=1
                    return("Shooter 1 destroyed Red")
        elif num_b_mis2>0:
            B_shoot2=random.randint(1, A_Shooter2)  #every GBASM fires or all remaining missiles fired if less than surviving GBASMs
            num_b_mis2-=1  #number of missiles decreases by number fired
            if B_shoot2>=S_Shields:  #if any of the missiles hit, B wins
                shields-=1
            if shields<0:  #if B runs out of missiles, R wins
                if B_shoot2>=Defense:  #if B runs out of missiles, R wins
                    winner+=1
                    return("Shooter 2 destroyed Red")
        elif num_b_mis3>0:
            B_shoot3=random.randint(1, A_Shooter3)  #every GBASM fires or all remaining missiles fired if less than surviving GBASMs
            num_b_mis3-=1  #number of missiles decreases by number fired
            if B_shoot3>=S_Shields:  #if any of the missiles hit, B wins
                shields-=1
            if shields<0:  #if B runs out of missiles, R wins
                if B_shoot3>=Defense:  #if B runs out of missiles, R wins
                    winner+=1
                    return("Shooter 3 destroyed Red")
        elif num_b_mis4>0:
            B_shoot4=random.randint(1, A_Shooter4)  #every GBASM fires or all remaining missiles fired if less than surviving GBASMs
            num_b_mis4-=1  #number of missiles decreases by number fired
            if B_shoot4>=S_Shields:  #if any of the missiles hit, B wins
                shields-=1
            if shields<0:  #if B runs out of missiles, R wins
                if B_shoot4>=Defense:  #if B runs out of missiles, R wins
                    winner+=1
                    return("Shooter 4 destroyed Red")
        elif num_b_mis5>0:
            B_shoot5=random.randint(1, A_Shooter5)  #every GBASM fires or all remaining missiles fired if less than surviving GBASMs
            num_b_mis5-=1  #number of missiles decreases by number fired
            if B_shoot5>=S_Shields:  #if any of the missiles hit, B wins
                shields-=1
            if shields<0:  #if B runs out of missiles, R wins
                if B_shoot5>=Defense:  #if B runs out of missiles, R wins
                    winner+=1
                    return("Shooter 5 destroyed Red")
        elif num_b_mis6>0:
            B_shoot6=random.randint(1, A_Shooter6)  #every GBASM fires or all remaining missiles fired if less than surviving GBASMs
            num_b_mis6-=1  #number of missiles decreases by number fired
            if B_shoot6>=S_Shields:  #if any of the missiles hit, B wins
                shields-=1
            if shields<0:  #if B runs out of missiles, R wins
                if B_shoot6>=Defense:  #if B runs out of missiles, R wins
                    winner+=1
                    return("Shooter 6 destroyed Red")
        elif num_b_mis7>0:
            B_shoot7=random.randint(1, A_Shooter7)  #every GBASM fires or all remaining missiles fired if less than surviving GBASMs
            num_b_mis7-=1  #number of missiles decreases by number fired
            if B_shoot7>=S_Shields:  #if any of the missiles hit, B wins
                shields-=1
            if shields<0:  #if B runs out of missiles, R wins
                if B_shoot7>=Defense:  #if B runs out of missiles, R wins
                    winner+=1
                    return("Shooter 7 destroyed Red")

        elif num_b_mis8>0:
            B_shoot8=random.randint(1, A_Shooter8)  #every GBASM fires or all remaining missiles fired if less than surviving GBASMs
            num_b_mis8-=1  #number of missiles decreases by number fired
            if B_shoot8>=S_Shields:  #if any of the missiles hit, B wins
                shields-=1
            if shields<0:  #if B runs out of missiles, R wins
                if B_shoot8>=Defense:  #if B runs out of missiles, R wins
                    winner+=1
                    return("Shooter 8 destroyed Red")
        elif num_b_mis9>0:
            B_shoot9=random.randint(1, A_Shooter9)  #every GBASM fires or all remaining missiles fired if less than surviving GBASMs
            num_b_mis9-=1  #number of missiles decreases by number fired
            if B_shoot9>=S_Shields:  #if any of the missiles hit, B wins
                shields-=1
            if shields<0:  #if B runs out of missiles, R wins
                if B_shoot9>=Defense:  #if B runs out of missiles, R wins
                    winner+=1
                    return("Shooter 9 destroyed Red")
        elif num_b_mis10>0:
            B_shoot10=random.randint(1, A_Shooter10)  #every GBASM fires or all remaining missiles fired if less than surviving GBASMs
            num_b_mis10-=1  #number of missiles decreases by number fired
            if B_shoot10>=S_Shields:  #if any of the missiles hit, B wins
                shields-=1
            if shields<0:  #if B runs out of missiles, R wins
                if B_shoot10>=Defense:  #if B runs out of missiles, R wins
                    winner+=1
                    return("Shooter 10 destroyed Red")
        else:
            winner+=1
            return("Out of shots")
n=10000
attack_values=[4,6,8,10,12,16,20]
st.title("Shot Simulator")
N_Shields=st.number_input("Enter number of defender’s shields",value=0,min_value=0, step=1)       
S_Shields=st.number_input("Enter strength of defender’s shields",value=0,min_value=0, step=1)  
Defense=st.number_input("Enter defender’s defense value",value=0,min_value=0, step=1)  
# Create a dropdown
selected_shooters = st.selectbox("Number of Shooters:", [1,2,3,4,5,6,7,8,9,10])        
n_shooters = selected_shooters        
if n_shooters>=1:
    A_Shooter1=st.selectbox("Sooter 1 Attack Value:", attack_values)
    S_Shooter1=st.number_input('Enter number of shots for Shooter 1:',value=0,min_value=0, step=1)
else:
    A_Shooter1=1
    S_Shooter1=0
if n_shooters>=2:
    A_Shooter2=st.selectbox("Sooter 2 Attack Value:", attack_values)
    S_Shooter2=st.number_input('Enter number of shots for Shooter 2:',value=0,min_value=0, step=1)
else:
    A_Shooter2=1
    S_Shooter2=0
if n_shooters>=3:
    A_Shooter3=st.selectbox("Sooter 3 Attack Value:", attack_values)
    S_Shooter3=st.number_input('Enter number of shots for Shooter 3:',value=0,min_value=0, step=1)
else:
    A_Shooter3=1
    S_Shooter3=0
if n_shooters>=4:
    A_Shooter4=st.selectbox("Sooter 4 Attack Value:", attack_values)
    S_Shooter4=st.number_input('Enter number of shots for Shooter 4:',value=0,min_value=0, step=1)
else:
    A_Shooter4=1
    S_Shooter4=0
if n_shooters>=5:
    A_Shooter5=st.selectbox("Sooter 5 Attack Value:", attack_values)
    S_Shooter5=st.number_input('Enter number of shots for Shooter 5:',value=0,min_value=0, step=1)
else:
    A_Shooter5=1
    S_Shooter5=0
if n_shooters>=6:
    A_Shooter6=st.selectbox("Sooter 6 Attack Value:", attack_values)
    S_Shooter6=st.number_input('Enter number of shots for Shooter 6:',value=0,min_value=0, step=1)
else:
    A_Shooter6=1
    S_Shooter6=0
if n_shooters>=7:
    A_Shooter7=st.selectbox("Sooter 7 Attack Value:", attack_values)
    S_Shooter7=st.number_input('Enter number of shots for Shooter 7:',value=0,min_value=0, step=1)
else:
    A_Shooter7=1
    S_Shooter7=0
if n_shooters>=8:
    A_Shooter8=st.selectbox("Sooter 8 Attack Value:", attack_values)
    S_Shooter8=st.number_input('Enter number of shots for Shooter 8:',value=0,min_value=0, step=1)
else:
    A_Shooter8=1
    S_Shooter8=0
if n_shooters>=9:
    A_Shooter9=st.selectbox("Sooter 9 Attack Value:", attack_values)
    S_Shooter9=st.number_input('Enter number of shots for Shooter 9:',value=0,min_value=0, step=1)
else:
    A_Shooter9=1
    S_Shooter9=0
if n_shooters>=10:
    A_Shooter10=st.selectbox("Sooter 10 Attack Value:", attack_values)
    S_Shooter10=st.number_input('Enter number of shots for Shooter 10:',value=0,min_value=0, step=1)
else:
    A_Shooter10=1
    S_Shooter10=0


Blue_Wins=0
Red_Wins=0
Blue1_Wins=0
Blue2_Wins=0
Blue3_Wins=0
Blue4_Wins=0
Blue5_Wins=0
Blue6_Wins=0
Blue7_Wins=0
Blue8_Wins=0
Blue9_Wins=0
Blue10_Wins=0
for i in range(n):
    sim= SHOT_SIM(A_Shooter1,S_Shooter1,
             A_Shooter2,S_Shooter2,
             A_Shooter3,S_Shooter3,
             A_Shooter4,S_Shooter4,
             A_Shooter5,S_Shooter5,
             A_Shooter6,S_Shooter6,
             A_Shooter7,S_Shooter7,
             A_Shooter8,S_Shooter8,
             A_Shooter9,S_Shooter9,
             A_Shooter10,S_Shooter10,
             N_Shields,S_Shields,Defense)
    if sim=="Shooter 1 destroyed Red":
        Blue_Wins+=1
        Blue1_Wins+=1
    if sim=="Shooter 2 destroyed Red":
        Blue_Wins+=1
        Blue2_Wins+=1
    if sim=="Shooter 3 destroyed Red":
        Blue_Wins+=1
        Blue3_Wins+=1
    if sim=="Shooter 4 destroyed Red":
        Blue_Wins+=1
        Blue4_Wins+=1
    if sim=="Shooter 5 destroyed Red":
        Blue_Wins+=1
        Blue5_Wins+=1
    if sim=="Shooter 6 destroyed Red":
        Blue_Wins+=1
        Blue6_Wins+=1
    if sim=="Shooter 7 destroyed Red":
        Blue_Wins+=1
        Blue7_Wins+=1
    if sim=="Shooter 8 destroyed Red":
        Blue_Wins+=1
        Blue8_Wins+=1
    if sim=="Shooter 9 destroyed Red":
        Blue_Wins+=1
        Blue9_Wins+=1
    if sim=="Shooter 10 destroyed Red":
        Blue_Wins+=1
        Blue10_Wins+=1
    if sim=="Out of shots":
        Red_Wins+=1

st.write("Blue's Win Percent:", round(Blue_Wins/n,2))
if n_shooters>=1:
    st.write("Proportion of iterations that shooter 1 destroyed red:", round(Blue1_Wins/n,2))
if n_shooters>=2:    
    st.write("Proportion of iterations that shooter 2 destroyed red:", round(Blue2_Wins/n,2))
if n_shooters>=3:    
    st.write("Proportion of iterations that shooter 3 destroyed red:", round(Blue3_Wins/n,2))
if n_shooters>=4:    
    st.write("Proportion of iterations that shooter 4 destroyed red:", round(Blue4_Wins/n,2))
if n_shooters>=5:    
    st.write("Proportion of iterations that shooter 5 destroyed red:", round(Blue5_Wins/n,2))
if n_shooters>=6:    
    st.write("Proportion of iterations that shooter 6 destroyed red:", round(Blue6_Wins/n,2))
if n_shooters>=7:    
    st.write("Proportion of iterations that shooter 7 destroyed red:", round(Blue7_Wins/n,2))
if n_shooters>=8:    
    st.write("Proportion of iterations that shooter 8 destroyed red:", round(Blue8_Wins/n,2))
if n_shooters>=9:    
    st.write("Proportion of iterations that shooter 9 destroyed red:", round(Blue9_Wins/n,2))
if n_shooters>=10:    
    st.write("Proportion of iterations that shooter 10 destroyed red:", round(Blue10_Wins/n,2))
    
    
    
