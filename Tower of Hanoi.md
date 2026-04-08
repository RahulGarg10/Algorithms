# Tower of Hanoi

Time Complexity: $O(2^n)$

Space Complexity: $O(n)$

``` python3
def tower_of_hanoi(N, from_rod, to_rod, aux_rod):
    count = 0
    def move_disk(N,from_rod,to_rod,aux_rod):
        nonlocal count
        if N==1:
            count+=1
            print("move disk " + str(N) + " from rod " + str(fromm) + " to rod " + str(to))
            return
        move_disk(N-1,from_rod,aux_rod,to_rod)
        count+=1
        print("move disk " + str(N) + " from rod " + str(fromm) + " to rod " + str(to))

        move_disk(N-1,aux_rod,to_rod,from_rod)
    move_disk(N,from_rod,to_rod,aux_rod)  
    return count
```
