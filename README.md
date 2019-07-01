# dox
Query DNS resolvers over different protocols

`dox` is a simple GUI tool for querying DNS servers.

It can be used as an ad-hoc query tool in much the same way
you might use `dig` or to survey the addresses different DNS
servers will return for the same query (and measure performance
differences between them).

## Protocols

Dox supports five different protocols

  * The resolver provided by the OS

  * Traditional [RFC 1035](https://tools.wordtothewise.com/rfc/1035) DNS over UDP
  
  * [RFC 7858](https://tools.wordtothewise.com/rfc/7858) DNS over TLS

  * [RFC 8484](https://tools.wordtothewise.com/rfc/8484) DNS over https POST

  * [RFC 8484](https://tools.wordtothewise.com/rfc/8484) DNS over https GET

It doesn't support JSON API DNS over HTTPS, only "wireformat" queries.

## Survey

Given a list of DNS resolvers and a list of URLs Dox can retrieve
the content of each URL using each resolver to locate it.

## Bugs

Many probably. It's prone to just log and ignore errors rather than
displaying them to the end user. This is not the tool you're looking
for as a sysadmin to diagnose a server, nor to show that a DNS resolver
is behavnig correctly.

## TODO

  * EDNS client subnet options

  * A better set of default resolvers - possibly snarfed from [stubby](https://github.com/getdnsapi/stubby)

  * End user docs