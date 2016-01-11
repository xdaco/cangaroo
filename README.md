# cangaroo
open source can bus analyzer

written by Hubert Denkmair <hubert@denkmair.de>

## changelog


### v0.1.2 (unreleased)
* fix device re-scan ("could not bind" console message)

### v0.1.1 released 2016-01-11
* change source structure to better fit debian packaging
* add debian packaging info

### v0.1 released 2016-01-10
initial release \o/



## todo

### backend
* allow for canfd frames
* support non-message frames in traces (e.g. markers)
* change message transfer from CanListeners to Backend (don't use signals/slots across threads?)
* implement plugin API
* embed python for scripting

### can drivers
* redo socketcan driver (clean qt/c++ implementation, suid binary for interface configuration)
* cannelloni support
* windows peak can driver
* windows vector driver

### import / export
* export to other file formats (e.g. Vector ASC, BLF)
* import CAN-Traces

### general ui
* maybe switch to docking window system

### logging subsystem
* redo, don't use qDebug() and friends
* show timestamps, log level etc. in log window

### trace window
* message filtering
* assign colors to can interfaces / messages
* limit displayed number of messages
* show error frames and other non-message frames

### raw message generator
* provide a simple way to generate raw can messages

### CanDB based generator
* generate can messages from candbs
* set signals according to value tables etc.
* provide generator functions for signal values
* allow scripting of signal values

### replay window
* replay can traces
* map interfaces in traces to available networks

### graph window
* test QCustomPlot
* allow for graphing of interface stats, message stats and signals

### packaging / deployment
* provide clean debian package
* gentoo ebuild script
* provide static linked binary
* make project build on windows
* add windows installer

