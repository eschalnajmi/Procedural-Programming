
# code details

EXE = ./bin/tictactoe
SRC = endGame.c initGame.c main.c playGame.c
OBJ = endGame.o initGame.o main.o playGame.o

# generic build details

CC     = gcc
CFLAGS = -std=c99 -Wall
CLIBS  = 
CLINK  = 

# compile to object code

%.o: %.c
	$(CC) -c $(CFLAGS) $(CLIBS) $< -o $@

# build executable: type 'make'

$(EXE): $(OBJ)
	$(CC) $(OBJ) $(CLINK) -o $(EXE) 

# clean up and remove object code and executable: type 'make clean'

clean:
	rm -f $(OBJ) $(EXE)

# dependencies

main.o: main.c endGame.h game.h initGame.h playGame.h
endGame.o: endGame.c endGame.h game.h playGame.h
initGame.o: initGame.c game.h
playGame.o: playGame.c endGame.h game.h playGame.h
