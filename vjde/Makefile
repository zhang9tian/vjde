

TARGET=plugin/vjde/preview4gtk.so


OUT_DIR=install

COMM_OBJS=$(OUT_DIR)/previewwindow.o $(OUT_DIR)/my_system.o

COMPILE= gcc `pkg-config --cflags gtk+-2.0`  -g -c 
COMPILE2= g++ `pkg-config --cflags gtk+-2.0`  -g -c -D_GTK_LINUX

#LINKS= 
LIBS=`pkg-config --libs gtk+-2.0`
LINK=g++

ALL	: $(TARGET)
	$(LINK)  -o $(TARGET) $(COMM_OBJS) $(LIBS) 

$(TARGET)	:$(COMM_OBJS)


$(OUT_DIR)/%.o 	: src/%.c
	$(COMPILE) -mms-bitfields -o "$(OUT_DIR)/$(*F).o" "$<"


$(OUT_DIR)/%.o 	: src/%.cpp
	$(COMPILE2)   -o "$(OUT_DIR)/$(*F).o" "$<"

clean	:
	rm $(OUT_DIR)/*.o
	rm $(TARGET)


so	: $(COMM_OBJS)
	g++ -shared -o plugin/vjde/preview4gtk.so $(COMM_OBJS) `pkg-config --cflags --libs gtk+-2.0` -D_GTK_LINUX




