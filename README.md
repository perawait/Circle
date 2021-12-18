# Circle




























import pygame

pygame.init()

display = pygame.display.set_mode((1280,720))

clock = pygame.time.Clock()
fps = 60
y = 350
x = 0
while True : 
    # check exit event
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            pygame.quit()
            exit()

    # check user input
    if pygame.key.get_pressed()[pygame.K_UP]:
        y -= 1
    if pygame.key.get_pressed()[pygame.K_DOWN]:
        y += 1

    # compute
    display.fill('white')
    pygame.draw.circle(display, 'red', (x, y), 50)
    

    # wait 
    clock.tick(fps)

    # display to player
    pygame.display.update()
    x += 1
