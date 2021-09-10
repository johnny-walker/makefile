# https://jasonblog.github.io/note/gunmake/makefilede_ji_ben_jie_gou.html
all: f1
	@echo recipe \`\`all\'\' executed.
f1: f2
	@echo process 1:
	touch f1
f2:
	@echo process 2:
	touch f2
clean:
	rm f1
	rm f2
.PHONY: clean