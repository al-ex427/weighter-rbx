# Weighter
Easy, simple syntax, for making a weight system


Syntax:

Create a weight class.
```lua
local WeightClass = weighter {
	{Name = "Low", Weight = 10};
	{Name = "Mid", Weight = 50};
	{Name = "High", Weight = 1000};
}

local WeightClass2 = weighter {
	{Name = "RandomA", Weight = 70};
	{Name = "RandomB", Weight = 15};
	{Name = "RandomC", Weight = 60};
}
```
Merge two weight classes
```
local CombinedClass = WeightClass + WeightClass2
```
Get a weight object of a weight class
```lua
print(CombinedClass.RandomA)
```
Multiply all weights in the weight class by a specified number
```
WeightClass = WeightClass*2
```
Convert a weight class into a string format which shows its properties
```
print(tostring(WeightClass))
```
Roll using weights
```
for i=1,100 do
	print(WeightClass())
end
```
Roll using %
```
for i=1,100 do
	print(WeightClass:RollNormalized())
end
```
