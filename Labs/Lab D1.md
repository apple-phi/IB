## 1.

```python
omega1=6.79  # rad per second
omega2=11.8  # rad per second
mode1shaperatio=0.47  #dimensionless ratio of alpha/beta for shape of mode 1
mode2shaperatio=-0.18 #dimensionless ratio of alpha/beta for shape of mode 2

gamma1=0.13 #1/seconds
gamma2=0.25 #1/seconds

# Using the function declarations from the notebook
makeplot(make_theoretical_data_with_damping(8,-23,4.2,1.8),My_Experiment_3)
```

![[D1-my-exp-3.png|600]]
## 2.

```python
# Using the function declarations from the notebook
plot_simulation_and_experiment(integrate([77*np.pi/180,0*np.pi /180,-2.5,2],5), My_Experiment_4)
```

![[D1-2nd-part.png|600]]
