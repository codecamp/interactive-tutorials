Tutorial
--------

### Знакомство

Numpy массивы являются отличной альтернативой спискам Python. Некоторые из ключевых преимуществ массивов Numpy состоят в том, что они быстры, просты в работе и дают пользователям возможность выполнять вычисления для целых массивов.

В следующем примере вы сначала создадите два списка Python. Затем вы импортируете пакет numpy и создадите numpy массивы из вновь созданных списков.

	# Create 2 new lists height and weight
	height = [1.87,  1.87, 1.82, 1.91, 1.90, 1.85]
	weight = [81.65, 97.52, 95.25, 92.98, 86.18, 88.45]

	# Import the numpy package as np
	import numpy as np

	# Create 2 numpy arrays from height and weight
	np_height = np.array(height)
	np_weight = np.array(weight)

# Выведите на экран тип np_height

    print(type(np_height))

### Поэлементные расчеты

Теперь мы можем выполнять поэлементные расчеты роста и веса. Например, вы можете взять все 6 наблюдений за ростом и весом, приведенные выше, и рассчитать ИМТ для каждого наблюдения с помощью одного уравнения. Эти операции очень быстрые и эффективные в вычислительном отношении. Они особенно полезны, когда у вас тысячи наблюдений в ваших данных.

<div data-Кодкамп-Упражнение data-height="225" data-encoded="true">
eyJsYW5ndWFnZSI6InB5dGhvbiIsInByZV9leGVyY2lzZV9jb2RlIjoiIiwic2FtcGxlIjoiIyBDYWxjdWxhdGUgYm1pXG5ibWkgPSBucF93ZWlnaHQgLyBucF9oZWlnaHQgKiogMlxuXG4jIFByaW50IHRoZSByZXN1bHRcbnByaW50KGJtaSkiLCJzb2x1dGlvbiI6IiMgQ2FsY3VsYXRlIGJtaVxuYm1pID0gbnBfd2VpZ2h0IC8gbnBfaGVpZ2h0ICoqIDJcblxuIyBQcmludCB0aGUgcmVzdWx0XG5wcmludChibWkpIiwic2N0Ijoic3VjY2Vzc19tc2coXCJHcmVhdCBqb2IhXCIpIn0=
</div>

### Создание подмножеств

Еще одна замечательная особенность массивов Numpy - возможность создавать подмножества. Например, если вы хотите узнать, какие наблюдения в нашем массиве ИМТ больше 23, мы могли бы быстро выяснить это с помощью подмножеств.

<div data-Кодкамп-Упражнение data-height="225" data-encoded="true">
eyJsYW5ndWFnZSI6InB5dGhvbiIsInByZV9leGVyY2lzZV9jb2RlIjoiIiwic2FtcGxlIjoiIyBGb3IgYSBib29sZWFuIHJlc3BvbnNlXG5ibWkgPiAyM1xuXG4jIFByaW50IG9ubHkgdGhvc2Ugb2JzZXJ2YXRpb25zIGFib3ZlIDIzXG5ibWlbYm1pID4gMjNdIiwic29sdXRpb24iOiIjIEZvciBhIGJvb2xlYW4gcmVzcG9uc2VcbmJtaSA+IDIzXG5cbiMgUHJpbnQgb25seSB0aG9zZSBvYnNlcnZhdGlvbnMgYWJvdmUgMjNcbmJtaVtibWkgPiAyM10iLCJzY3QiOiJzdWNjZXNzX21zZyhcIkdyZWF0IGpvYiFcIikifQ==
</div>

Упражнение
--------

Сначала преобразуйте список весов из списка в массив Numpy. Затем переведите все веса из килограммов в фунты. Используйте скалярное преобразование 2,2 фунта за килограмм. Наконец, выведите получившийся массив весов в фунтах.

<div data-Кодкамп-Упражнение data-height="300" data-encoded="true">
eyJsYW5ndWFnZSI6InB5dGhvbiIsInByZV9leGVyY2lzZV9jb2RlIjoiIiwic2FtcGxlIjoid2VpZ2h0X2tnID0gWzgxLjY1LCA5Ny41MiwgOTUuMjUsIDkyLjk4LCA4Ni4xOCwgODguNDVdXG5cbmltcG9ydCBudW1weSBhcyBucFxuXG4jIENyZWF0ZSBhIG51bXB5IGFycmF5IG5wX3dlaWdodF9rZyBmcm9tIHdlaWdodF9rZ1xuICAgIFxuXG4jIENyZWF0ZSBucF93ZWlnaHRfbGJzIGZyb20gbnBfd2VpZ2h0X2tnXG5cbiMgUHJpbnQgb3V0IG5wX3dlaWdodF9sYnMiLCJzb2x1dGlvbiI6IndlaWdodF9rZyA9IFs4MS42NSwgOTcuNTIsIDk1LjI1LCA5Mi45OCwgODYuMTgsIDg4LjQ1XVxuXG5pbXBvcnQgbnVtcHkgYXMgbnBcblxuIyBDcmVhdGUgYSBudW1weSBhcnJheSBucF93ZWlnaHRfa2cgZnJvbSB3ZWlnaHRfa2dcbm5wX3dlaWdodF9rZyA9IG5wLmFycmF5KHdlaWdodF9rZylcblxuIyBDcmVhdGUgbnBfd2VpZ2h0X2xicyBmcm9tIG5wX3dlaWdodF9rZ1xubnBfd2VpZ2h0X2xicyA9IG5wX3dlaWdodF9rZyAqIDIuMlxuXG4jIFByaW50IG91dCBucF93ZWlnaHRfbGJzXG5wcmludChucF93ZWlnaHRfbGJzKSIsInNjdCI6InN1Y2Nlc3NfbXNnKFwiR3JlYXQgam9iIVwiKSJ9
</div>

Tutorial Code
-------------

Expected Output
---------------

Solution
--------
