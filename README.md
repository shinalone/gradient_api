## ***The document of [gradient_api]()*** ##


- *Usage:*

```python
>>> from gradient_api import gradient

>>> r1 = gradient.generate_1d(expr_or_poly1d='x**2+1')
>>> r2 = gradient.generate_2d(expr_or_poly1d=[1,0,1])

>>> print(r1 == r2)
True

>>> print(r1)
{'X': -0.00011417981541647683, 'Y': 1.0000000130370303, 'Gradient': -0.00022835963083295366, 'Numloop': 51}
```

```python
>>> trainData = pandas.DataFrame(numpy.array([[1,3,5,7],[2,4,6,8]]))
>>> r3 = gradient.generate_2d(trainData)
>>> print(r3)

{'Gradient': array([-1020.54, -1589.21, -3630.29, -5671.37]),
 'Linear_Coef': array([-16.94, -38.6 , -60.26]),
 'Linear_Intercept': -10.83,
 'Numloop': 2,
 'Y': 263786.0329,
 'theta': array([-10.83, -16.94, -38.6 , -60.26])}
```

- *Tips:*
```python
generate_1d(expr_or_poly1d,init_x=-0.5,step=0.01,num_iters=1e4,showPlot=False,xlimArr=None,ylimArr=None)
```

```python
generate_2d(dataFrame,step=0.1,num_iters=1e4)
```


- *[gradient.generate_1d(expr_or_poly1d='x**2+1', showPlot=True)]()*

![gradient_11](https://i.imgur.com/Mw4LmdE.gif)
