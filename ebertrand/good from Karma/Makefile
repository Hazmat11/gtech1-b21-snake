CC=g++
# Adapt the variables below to your needs:
EXE=snake
CPP=main.cpp apple.cpp MainSDLWindow.cpp snake.cpp score.cpp
HPP=apple.hpp MainSDLWindow.hpp snake.hpp score.hpp

# The default is build the executable file:
default: $(EXE)

# The executable file must be rebuilt if source files changed:
$(EXE): $(CPP) $(HPP)
	$(CC) $(CPP) -l SDL2 -o $(EXE)

# Run of the (always up-to-date) executable:
run: $(EXE)
	./$(EXE)

# Build the UML diagram as a PNG image:
uml/classes.png: *.hpp
	./uml/mk_uml.sh uml/classes.png *.hpp

# Count the number of lines of code:
nblines:
	@wc -l $(CPP) $(HPP)