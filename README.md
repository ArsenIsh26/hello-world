# hello-world
import matplotlib.pyplot as plt

with open('new 1.txt', 'r') as file:
    lines = file.readlines()

x = []
y = []

for line in lines:
    values = line.strip().split()
    values = [sub.replace(',', '.') for sub in values]
    x.append(float(values[0]))
    y.append(float(values[1]))


mean_y = sum(y) / len(y)
print(mean_y)


x1 = []
y1 = []
for line in lines:
    values = line.strip().split()
    values = [sub.replace(',', '.') for sub in values]
    x0 = (float(values[0]))
    y0 = (float(values[1]))
    if y0 <= mean_y:
        x1.append(x0)
        y1.append(y0)

plt.plot(x1, y1)
plt.xlabel('Значення x')
plt.ylabel('Значення y')
plt.title('Графік')
plt.show()
