class Solution:
    def minMovesToSeat(self, seats: List[int], students: List[int]) -> int:
        seats.sort()
        students.sort()
        x = 0
        for seat , student in zip(seats,students):
            x += abs(seat-student)
        return x
