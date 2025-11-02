GPP = g++

SRC_DIR = src
LOG_DIR = logs
BUILD_DIR = build
BIN_DIR = bin

EXEC = $(BIN_DIR)/pim_gl

SOURCES = $(wildcard $(SRC_DIR)/*.cpp)
OBJECTS = $(SOURCES:$(SRC_DIR)%.cpp=$(BUILD_DIR)%.o)

CFLAGS = -g -Og -Wall -Wextra -pedantic -fsanitize=address
LDFLAGS = -g -Og -Wall -Wextra -pedantic -fsanitize=address 

.PHONY: all clean install

all: $(EXEC)

$(EXEC): $(OBJECTS)
	$(GPP) $(OBJECTS) -o $(EXEC) $(LDFLAGS)

$(BUILD_DIR)/%.o: $(SRC_DIR)/%.cpp
	$(GPP) -c $< -o $@ $(CFLAGS)

clean:
	-rm $(EXEC)
	-rm $(OBJECTS)

