def calculate_errors():
    print("--- Вычисление абсолютной и относительной погрешности ---")
    
    try:
        # 1. Входные данные: принимается 2 числа
        x_input = input("Введите точное значение x: ")
        x_approx_input = input("Введите приближенное значение x_approx: ")
        
        x = float(x_input)
        x_approx = float(x_approx_input)

        # 2. Нахождение абсолютной погрешности delta = |x - x*|
        delta = abs(x - x_approx)

        # 3. Нахождение относительной погрешности delta_relative = delta / x
        # Проверка на деление на ноль (пункт 5: Вывод ошибки)
        if x == 0:
            print("\nОшибка: Точное значение x не может быть равно нулю (деление на ноль невозможно).")
            return

        delta_relative = delta / abs(x) # Берем abs(x), чтобы относительная погрешность была положительной

        # 4. Вывод результата delta и delta_relative
        print(f"\nАбсолютная погрешность (delta): {delta}")
        print(f"Относительная погрешность (delta_relative): {delta_relative}")

    except ValueError:
        # 5. Вывод ошибки, если введены не числа
        print("\nОшибка: Пожалуйста, введите корректные числовые значения.")

# Запуск программы
if __name__ == "__main__":
    calculate_errors()