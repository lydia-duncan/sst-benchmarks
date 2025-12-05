CXX=$(shell sst-config --CXX)
CXXFLAGS=$(shell sst-config --ELEMENT_CXXFLAGS) -g
LDFLAGS=$(shell sst-config --ELEMENT_LDFLAGS)

SRCS=Node.cpp

all: libloadImbalance2.so install

libloadImbalance2.so: $(SRCS)
	$(CXX) $(CXXFLAGS) $(LDFLAGS) -o $@ $^

install:
	sst-register loadImbalance2 loadImbalance2_LIBDIR=$(CURDIR)

clean:
	rm -rf libloadImbalance2.so
	sst-register -u loadImbalance2
	rm -r *.json *.tmp *.time *.out
