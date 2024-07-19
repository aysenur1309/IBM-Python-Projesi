# IBM-Python-Projesi
Python Kullanılarak Minimum Öklid Mesafesinin Hesaplanması
import math

# Noktaların Tanımlanması
points = [(0, 1), (2, 3), (4, 5), (6, 7)]

# Öklid Mesafesi için Bir Fonksiyon Yazma
def euclideanDistance(point1, point2):
    return math.sqrt((point1[0] - point2[0]) ** 2 + (point1[1] - point2[1]) ** 2)

# Mesafelerin Hesaplanması
distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        dist = euclideanDistance(points[i], points[j])
        distances.append(dist)

# Minimum Mesafenin Bulunması
min_distance = min(distances)
print(f"Minimum mesafe: {min_distance}")
