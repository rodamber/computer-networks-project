EXEC=user

all: $(EXEC)

run: all
	./$(EXEC) 12345

$(EXEC): *.py
	zip -r $(EXEC).zip $^
	echo '#!/usr/bin/env python3' | cat - $(EXEC).zip > $(EXEC)
	rm $(EXEC).zip
	chmod +x $(EXEC)

clean:
	rm -f $(EXEC)
	rm -rf __pycache__
