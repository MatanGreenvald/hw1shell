CC = gcc
CFLAGS = -Wall -g -MMD -MP
SRC = hw1shell.c shell.c
OBJ = $(SRC:.c=.o)
DEP = $(OBJ:.o=.d)
TARGET = hw1shell

# Default target to build the program
all: $(TARGET)

# Link object files to create the executable
$(TARGET): $(OBJ)
	$(CC) $(OBJ) -o $(TARGET)

# Compile source files into object files
%.o: %.c
	$(CC) $(CFLAGS) -c $< -o $@

# Include automatically generated dependency files
-include $(DEP)

# Clean up build files
clean:
	rm -f $(OBJ) $(DEP) $(TARGET)