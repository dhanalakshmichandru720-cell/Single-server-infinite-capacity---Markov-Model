# Single server with infinite capacity (M/M/1):(oo/FIFO)

## Procedure :

![imAGE](2.png)

## Program
```
arr_time=float(input("Enter the mean inter arrival time of objects from Feeder (in secs): "))
ser_time=float(input("Enter the mean  inter service time of Lathe Machine (in secs) :  "))
Robot_time=float(input("Enter the Additional time taken for the Robot (in secs) :  "))
lam=1/arr_time
mu=1/(ser_time+Robot_time)
print("--------------------------------------------------------------")
print("Single Server with Infinite Capacity - (M/M/1):(oo/FIFO)")
print("--------------------------------------------------------------")
print(f"The mean arrival rate per second : {lam:.2f}")
print(f"The mean service rate per second : {mu:.2f}")
if (lam <  mu):
    Ls=lam/(mu-lam)
    Lq=Ls-lam/mu
    Ws=Ls/lam
    Wq=Lq/lam
    print(f"Average number of objects in the system : {Ls:.2f}")
    print(f"Average number of objects in the conveyor :  {Lq:.2f}")
    print(f"Average waiting time of an object in the system : {Ws:.2f} secs")
    print(f"Average waiting time of an object in the conveyor : {Wq:.2f} secs")
    print(f"Probability that the system is busy : {(lam/mu):.2f}" )
    print(f"Probability that the system is empty : {(1-lam/mu):.2f}" )
else:
    print("Warning! Objects Over flow will happen in the conveyor")
print("---------------------------------------------------------------")
```
## Output :

<img width="769" height="344" alt="Screenshot 2026-05-24 211545" src="https://github.com/user-attachments/assets/06e80ed3-9275-4cca-b8e6-3dcac789391f" />

## Result :

