
Sure, I can help you with that. Here is a simple code for a 2D game where a bird can fly:

Python
import pygame

# Initialize the game
pygame.init()

# Create the screen
screen = pygame.display.set_mode((640, 480))

# Load the bird image
bird_image = pygame.image.load("bird.png")

# Create the bird object
bird = pygame.Rect(200, 200, 50, 50)

# Game loop
while True:
    # Check for events
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            quit()

    # Move the bird
    if event.type == pygame.KEYDOWN and event.key == pygame.K_SPACE:
        bird.y -= 20

    # Draw the background
    screen.fill((255, 255, 255))

    # Draw the bird
    screen.blit(bird_image, bird)

    # Update the display
    pygame.display.flip()
