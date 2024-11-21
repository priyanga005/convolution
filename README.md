import numpy as np

def linear_convolution(x, h):
    """
    Perform linear convolution between two sequences x and h.
    
    Parameters:
    x : list or array
        The input signal.
    h : list or array
        The impulse response.
    
    Returns:
    y : array
        The result of the convolution.
    """
    # Length of the output sequence
    len_y = len(x) + len(h) - 1
    # Initialize the output sequence
    y = np.zeros(len_y)
    
    # Perform convolution
    for i in range(len(x)):
        for j in range(len(h)):
            y[i + j] += x[i] * h[j]
    
    return y

# Example usage
x = [1, 2, 3]  # Input sequence
