CFLAGS += -Wall -Werror

all: l2tp_client

%.o: %.c
        $(CC) $(CFLAGS) -c -I. -o $@ $<

l2tp_client: l2tp_client.o libasyncns/asyncns.o
        $(CC) $(LDFLAGS) -o $@ $^ -lpthread -lnl -lrt -lresolv

clean:
        rm -rf *.o l2tp_client
