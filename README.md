# hw3_quicksort
def quick_sort(array):
    if len(array) <= 1:
        return array
    else:
        pivot = array[len(array) // 2]
        left = [x for x in array if x < pivot]
        middle = [x for x in array if x == pivot]
        right = [x for x in array if x > pivot]
        print(f"Left: {left},   Pivot: {middle},   Right: {right}")
        return quick_sort(left) + middle + quick_sort(right)

# 上課範例
example = [33, 67, 8, 13, 54, 119, 3, 84, 25, 41]
print("Input array:", example)
sorted_array = quick_sort(example)
print("Sorted array:", sorted_array)

# 執行結果
Input array: [33, 67, 8, 13, 54, 119, 3, 84, 25, 41]
Left: [33, 67, 8, 13, 54, 3, 84, 25, 41],   Pivot: [119],   Right: []
Left: [33, 8, 13, 3, 25, 41],   Pivot: [54],   Right: [67, 84]
Left: [],   Pivot: [3],   Right: [33, 8, 13, 25, 41]
Left: [8],   Pivot: [13],   Right: [33, 25, 41]
Left: [],   Pivot: [25],   Right: [33, 41]
Left: [33],   Pivot: [41],   Right: []
Left: [67],   Pivot: [84],   Right: []
Sorted array: [3, 8, 13, 25, 33, 41, 54, 67, 84, 119]
