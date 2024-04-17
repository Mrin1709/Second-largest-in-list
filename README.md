def second_largest(lst):
    
    if len(lst) < 2:
        return "List should have at least two elements"
    
    
    first_largest = max(lst[0], lst[1])
    second_largest = min(lst[0], lst[1])
    
    for num in lst[2:]:
        if num > first_largest:
            second_largest = first_largest
            first_largest = num
        elif num > second_largest and num != first_largest:
            second_largest = num
    
    return second_largest

numbers = [5, 2, 8, 1, 9, 3]

result = second_largest(numbers)

print("Second largest number in the list:", result)
