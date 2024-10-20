def find_position(heights, petya_height):
    position = 0
    for height in heights:
        if height > petya_height:
            position += 1
        else:
            position += 1  # Увеличиваем позицию на 1, так как Петя должен встать после тех, кто с ним равен
            break
            
    return position

# Читаем входные данные
input_data = input("Введите рост людей в строю (через пробел): ")
heights = list(map(int, input_data.split()))
petya_height = int(input("Введите рост Пети: "))

# Ищем позицию
result = find_position(heights, petya_height)

# Выводим результат
print(result)
