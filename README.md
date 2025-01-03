# Minimum-klid-Mesafesinin-Hesaplanmas-
import math

def euclideanDistance(point1, point2):
  x1, y1 = point1
  x2, y2 = point2
  distance = math.sqrt((x2 - x1)**2 + (y2 - y1)**2)
  return distance

points = [(1, 2), (4, 6), (10, 12), (15, 18), (2, 1)]

distances = []
for i in range(len(points)):
  for j in range(i + 1, len(points)):
    distance = euclideanDistance(points[i], points[j])
    distances.append(distance)

if distances:
    min_distance = min(distances)
    print("Minimum Öklid Mesafesi:", min_distance)
else:
    print("Hiç mesafe hesaplanmadı. Nokta listesi çok küçük olabilir.")
