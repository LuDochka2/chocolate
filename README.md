# chocolateimport matplotlib.pyplot as plt
import matplotlib.patches as patches

def draw_milk_chocolate():
    # Create a figure and axis
    fig, ax = plt.subplots()

    # Draw the chocolate bar (a brown rectangle)
    chocolate_bar = patches.Rectangle((0.1, 0.3), 0.8, 0.4, linewidth=1, edgecolor='black', facecolor='#8B4513')
    ax.add_patch(chocolate_bar)

    # Draw the segments of the chocolate bar
    num_segments = 4  # Number of segments in the chocolate bar
    for i in range(1, num_segments):
        # Vertical lines for the segments
        ax.plot([0.1 + i * 0.8 / num_segments, 0.1 + i * 0.8 / num_segments], [0.3, 0.7], color='black', linewidth=2)
    
    # Set the aspect ratio to be equal
    ax.set_aspect('equal')

    # Set the limits and remove axes
    plt.xlim(0, 1)
    plt.ylim(0, 1)
    plt.axis('off')

    # Show the plot
    plt.show()

# Draw the milk chocolate bar
draw_milk_chocolate()
