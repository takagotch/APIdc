ruby -rpp -rsocket -e 'pp Socket.getaddinfo("www.ruby-lang.org", "http")'

ruby -rpp -rsocket -e 'pp Addrinfo.getaddinfo("www.ruby-lang.org", "http")'

//Clang addinfo
struct addinfo {
  int ai_flags;
  int ai_family;
  int ai_socketype;
  int ai_protocol;
  socklen_t ai_addrlen;
  struct sockaddr *ai_addr;
  char *ai_canonname;
  struct addinfo *ai_next;
}

ruby -rpp -rsocket -e'BasicSocket.do_not_reverse_lookup = false pp Socket.getaddinfo("www.ruby-lang.org", "http")'

TCPSocket.open("www.ruby-lang.org", 80) {|s|
  p s.getsockename #=>
  p s.getpeername #=>
}

TCPSocket.open("www.ruby-lang.org", 80){|s|
  p s.local_address #=>
  p s.remote_address #=>
}