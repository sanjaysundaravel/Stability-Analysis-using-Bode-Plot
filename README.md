# Stability-Analysis-using-Bode-Plot

## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 

## Apparatus Required:
Computer with MATLAB software

## Theory:
![image 5(1](https://github.com/user-attachments/assets/e1a05b28-fae2-44a1-ada3-57f9c14a43cf)
![image 5 (2](https://github.com/user-attachments/assets/0bcc4ab8-8a3f-4856-ae24-c5fc135ebe44)




## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program:

```
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
bode(sys)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
    disp('stable')
elseif(Wpc == Wgc)
    disp('marginally stable')
else
    disp('unstable')
end
```

## Output:

<img width="707" height="630" alt="image" src="https://github.com/user-attachments/assets/c43c55ab-6b64-4424-827f-8ff179b29b97" />


## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12 <br>
Phase Margin = 60 <br>
Gain crossover frequency = 0.907 <br>
Phase crossover frequency = 4.4721 <br>
The system is stable.
