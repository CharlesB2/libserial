SIPFILES = \
	SerialPort.sip \
	SerialPortConstants.sip \
	exception.sip \
	libserial.sip \
	stdexcept.sip \
	string.sip \
	vector.sip 

EXTRA_DIST = \
	configure.py.in \
	recv_test.py \
	send_test.py \
	$(SIPFILES)

all: libserial.so

libserial.so: Makefile.sip @top_srcdir@/src/libserial.la
	make -f Makefile.sip

Makefile.sip: configure.py $(SIPFILES)
	python ./configure.py

clean-local: Makefile.sip
	make -f Makefile.sip clean

CLEANFILES = \
	Makefile.sip \
	libserial.sbf \
	sipAPIlibserial.h \
	siplibserialLibSerial.cpp \
	siplibserialLibSerialBaudRate.cpp \
	siplibserialLibSerialCharacterSize.cpp \
	siplibserialLibSerialFlowControl.cpp \
	siplibserialLibSerialParity.cpp \
	siplibserialLibSerialStopBits.cpp \
	siplibserialSerialPort.cpp \
	siplibserialcmodule.cpp \
	siplibserialstd.cpp \
	siplibserialstdexception.cpp \
	siplibserialstdinvalid_argument.cpp \
	siplibserialstdios_base \
	siplibserialstdlogic_error.cpp \
	siplibserialstdruntime_error.cpp \
	siplibserialstdstring.cpp \
	siplibserialstdvector1300.cpp \
	siplibserialstdvector1800.cpp \
	siplibserialstdvector1900.cpp \
	siplibserialstdvector2400.cpp
