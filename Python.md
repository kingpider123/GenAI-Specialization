# Class
* Blueprint for creating something
```
class Circle(object):
    def __init__(self,radius=3,color='blue'):
        self.radius = radius
        self.color = color
    
    def add_radius(self,r):
        self.radius=self.radius + r
```
# Objects
* The actual thing created from the blueprint
```
RedCircle = Circle(10,"red")
RedCircle.radius
RedCircle.color
RedCircle.add_radius(5)

```