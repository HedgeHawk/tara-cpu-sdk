#Makefile to generate the TaraDisparityViewer Application
#While executing make, TaraDisparityViewer binary will be generated

#Variables and Constants
CC=g++
OUTPUT=TaraDisparityViewer
COMMON_LIBS_PREFIX=./../../../common

#Formatting options
RED=\033[0;31m
GREEN=\033[0;32m
BLUE=\033[0;34m
NC=\033[0m # No Color
BOLD=\033[1m

#Includes and libs
CFLAGS=-I $(COMMON_LIBS_PREFIX)/include `pkg-config --cflags glib-2.0`
ECON_LIBS=-L $(COMMON_LIBS_PREFIX)/Tara -lecon_tara -L $(COMMON_LIBS_PREFIX)/xunit -lecon_xunit 
OPENCV_LIBS=`pkg-config --cflags --libs opencv4`


#Building Targets
default: $(OUTPUT)
 
$(OUTPUT): DisparityViewer.cpp common_libs
	@echo "\n${BLUE}${BOLD}Building $(OUTPUT) Application${NC}"
	@$(CC) $< -o $@ $(CFLAGS) $(ECON_LIBS) $(OPENCV_LIBS)
	@echo "\n${GREEN}${BOLD}$(OUTPUT) Application build completed${NC}"		

common_libs:
	@make -C $(COMMON_LIBS_PREFIX)

clean:
	@echo "\n${BLUE}${BOLD}Removing $(OUTPUT) Application${NC}"
	@rm $(OUTPUT) 
	@echo "\n${GREEN}${BOLD}$(OUTPUT) Application removed${NC}"		
