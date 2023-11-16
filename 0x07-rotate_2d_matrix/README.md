#!/usr/bin/python3
'''2D matrix'''


def rotate_2d_matrix(matrix):
    '''rotates a 2d matrix 90° clockwise
    Returns: Nothing'''
    left, right = 0, len(matrix) - 1

    while left < right:
        for i in range(right - left):
            top, bottom = left, right
            # save topleft  value
            topLeft = matrix[top][left + i]
            # move bottom left to top left
            matrix[top][left + i] = matrix[bottom - i][left]
            # move bottom right to bottom left
            matrix[bottom - i][left] = matrix[bottom][right - i]
            # move top right to bottom right
            matrix[bottom][right - i] = matrix[top + i][right]
            # move top left to top right
            matrix[top + i][right] = topLeft
        right -= 1
        left += 1



0x07. Rotate 2D Matrix
Algorithm
Python
 By: Jesse Hedden, Software Engineer
 Weight: 1
 Project will start Nov 13, 2023 5:00 AM, must end by Nov 17, 2023 5:00 AM
 Checker was released at Nov 14, 2023 5:00 AM
 An auto review will be launched at the deadline
Requirements
General
Allowed editors: vi, vim, emacs
All your files will be interpreted/compiled on Ubuntu 20.04 LTS using python3 (version 3.8.10)
All your files should end with a new line
The first line of all your files should be exactly #!/usr/bin/python3
A README.md file, at the root of the folder of the project, is mandatory
Your code should use the pycodestyle style (version 2.8.0)
You are not allowed to import any module
All modules and functions must be documented
All your files must be executable
