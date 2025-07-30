# Performance Optimization Module

## Подготовка тестовых файлов

Для работы с `module_10_5.py` необходимо создать тестовые файлы:

```bash
# Создайте тестовые файлы разного размера
echo "Test content for file 1" > "file 1.txt"
echo "Test content for file 2" > "file 2.txt"  
echo "Test content for file 3" > "file 3.txt"
echo "Test content for file 4" > "file 4.txt"

# Или создайте файлы большего размера для тестирования производительности:
# Примерно 1MB каждый
python3 -c "
import random
import string

for i in range(1, 5):
    with open(f'file {i}.txt', 'w') as f:
        content = ''.join(random.choices(string.ascii_letters + string.digits + ' \n', k=1000000))
        f.write(content)
"
```

## Описание

Этот модуль демонстрирует различия в производительности между:
- Последовательным чтением файлов
- Многопоточным чтением файлов

Тестовые файлы не включены в репозиторий для экономии места.