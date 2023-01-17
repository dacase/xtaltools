#  Very simple Makefile.  Change the following flags if needed.


CC = gcc
CFLAGS = -g -O3 -Wno-unused-result
LDFLAGS = 
BINDIR = .

.c.o:
	@echo "[XTALUTIL]  CC $<"
	@$(CC) -c $(CFLAGS) -o $@ $< 

OBJS = crdmanip.o grid.o matrix.o pdbRead.o rand2.o topRead.o vector.o

xtalutil: $(BINDIR)/ChBox $(BINDIR)/UnitCell \
     $(BINDIR)/AddToBox $(BINDIR)/PropPDB

$(BINDIR)/AddToBox: AddToBox.o $(OBJS)
	@echo "[XTALUTIL]  CC $@"
	@$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $^ -lm

$(BINDIR)/ChBox: ChBox.o $(OBJS)
	@echo "[XTALUTIL]  CC $@"
	@$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $^ -lm

$(BINDIR)/CheckMD: CheckMD.o $(OBJS)
	@echo "[XTALUTIL]  CC $@"
	@$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $^ -lm

$(BINDIR)/PropPDB: PropPDB.o $(OBJS)
	@echo "[XTALUTIL]  CC $@"
	@$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $^ -lm

$(BINDIR)/UnitCell: UnitCell.o $(OBJS)
	@echo "[XTALUTIL]  CC $@"
	@$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $^ -lm

$(BINDIR)/pdb2rdf: pdb2rdf.o $(OBJS)
	@echo "[XTALUTIL]  CC $@"
	@$(CC) $(CFLAGS) $(LDFLAGS) -o $@ $^ -lm

uninstall: clean
	/bin/rm -f $(BINDIR)/AddToBox $(BINDIR)/ChBox \
       $(BINDIR)/PropPDB $(BINDIR)/UnitCell

clean:
	/bin/rm -f *.o

