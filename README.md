# super-octo-chainsaw
//Öklid mesafesi
import math

# Noktaları içeren liste
points = [(1, 2), (4, 6), (7, 8), (2, 3), (5, 9)]

# Öklid mesafesi hesaplayan fonksiyon
def euclideanDistance(p1, p2):
    return math.sqrt((p2[0] - p1[0])**2 + (p2[1] - p1[1])**2)

# Tüm nokta çiftleri arasındaki mesafeleri hesapla
distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distances.append(euclideanDistance(points[i], points[j]))

# Minimum mesafeyi bul ve yazdır
min_distance = min(distances)
print("Minimum Öklid Mesafesi:", min_distance)
