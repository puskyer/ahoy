PREFIX  = /usr
CFLAGS  ?= -g -Wall -Wno-deprecated-declarations -O2
LIBS    = -lSDL2 -lSDL2_image
OBJS    = ahoy.o
TARGET  = ahoy

$(TARGET): $(OBJS)
	$(CXX) $(LDFLAGS) -o $@ $^ $(LIBS)

%.o: %.cpp
	$(CXX) $(CPPFLAGS) $(CFLAGS) $(DEFINES) -o $@ -c $<

install: $(TARGET)
	mkdir -p $(DESTDIR)$(PREFIX)/bin
	install -p -m 755 $(TARGET) $(DESTDIR)$(PREFIX)/bin

clean:
	rm -f $(OBJS) $(TARGET) *~
