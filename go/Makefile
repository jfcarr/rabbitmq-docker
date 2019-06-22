RECEIVEDIR = receive-app
SENDDIR = send-app

default:
	@echo 'Targets'
	@echo '  receive    Build the receive application.'
	@echo '  send       Build the send application.'
	@echo '  clean      Remove built binaries.'

receive:
	@cd $(RECEIVEDIR) && go build receive.go

send:
	@cd $(SENDDIR) && go build send.go

clean:
	@-rm -f $(RECEIVEDIR)/receive
	@-rm -f $(SENDDIR)/send
