# Stateful Vs Stateless Firewalls
TCP connection based protocol established btw 2 devices using a random port on a client and a known port on the server. Runs on top of IP. Once established, the connection is bidirectional.
HTTPS --> TCP/443
HTTP --> TCP/

Every connection has:
- request
- response

Client chooses a temporary/ephemeral source port, initiates a connection on the Server on a well known destination port HTTPS tcp/443 (REQUEST)
Server responds back using source port of tcp/443 and the destination ephemeral port picked by client (RESPONSE) 

## Stateless Firewalls

Stateless firewalls require two rules per connection (1 IN, 1 OUT).

Stateless firewalls are an older technology that require more admin overhead, but they do come with the benefit of being able to better control both sides of traffic flow.

## Stateful Firewall

Stateful firewalls are intelligent enough to identify the REQUEST and RESPONSE components of a connection as being related.

With stateful firewalls, allowing a request generally means that the response will be automatically allowed as well.

Stateful firewalls are a modern technology that require less admin overhead.
