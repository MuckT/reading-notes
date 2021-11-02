# 401 Socket.io

## Vocabulary Terms
| Term | Definition |
| ---- | ---- |
| Observer Pattern | The observer pattern is a software design pattern in which an object, named the subject, maintains a list of its dependents, called observers, and notifies them automatically of any state changes, usually by calling one of their methods. |
| Listener | A callback subroutine that handles inputs received in a program. |
| Event Handler | Code that will run when an event fires |
| Event Driven Programming | A programming paradigm in which the flow of the program is determined by events such as user actions (mouse clicks, key presses), sensor outputs, or message passing from other programs or threads. |
| Event Loop | A programming construct or design pattern that waits for and dispatches events or messages in a program. The event loop works by making a request to some internal or external "event provider" (that generally blocks the request until an event has arrived), then calls the relevant event handler ("dispatches the event"). The event loop is also sometimes referred to as the message dispatcher, message loop, message pump, or run loop.|
| Event Queue a.k.a Message queue | message queues and mailboxes are software-engineering components typically used for inter-process communication (IPC), or for inter-thread communication within the same process. They use a queue for messaging – the passing of control or of content. |
| Call Stack | A stack data structure that stores information about the active subroutines of a computer program. This kind of stack is also known as an execution stack, program stack, control stack, run-time stack, or machine stack. |
| Emit/Raise/Trigger | Functions in event-driven coding are functions that discharge a specific event. |
| Publish–subscribe pattern | A messaging pattern where senders of messages, called publishers, do not program the messages to be sent directly to specific receivers, called subscribers, but instead categorize published messages into classes without knowledge of which subscribers, if any, there may be. Similarly, subscribers express interest in one or more classes and only receive messages that are of interest, without knowledge of which publishers, if any, there are. |
| database | An organized collection of structured information, or data, typically stored electronically in a computer system. A database is usually controlled by a database management system (DBMS). Together, the data and the DBMS, along with the applications that are associated with them, are referred to as a database system, often shortened to just database. |
| Full duplex (FDX) | A full-duplex (FDX) system allows communication in both directions, and, unlike half-duplex, allows this to happen simultaneously. |

### What is the benefit of transforming data into packets?

This allows the network to accommodate various bandwidths, multiple routes to a destination, and to retransmit the pieces of data which are interrupted or lost.

### UDP is often refereed to as a connectionless protocol. Why is this?

There are no pre-established relationships in order to communicate. There is no notification of a failure, nor can we make assumptions about the sequence of delivery.

### Can a socket server application have multiple socket connections?

A web socket server can have multiple socket connections / clients.

### Can a socket connection application be connected to multiple socket servers?

Yes, a socket connection can be connected to multiple socket servers.

### Can an application be both a socket server and a socket connection?

No, ideally, because we only want to one have one global event pool. This helps in the separation of concerns.

## Sources

[Observer Pattern](https://en.wikipedia.org/wiki/Observer_pattern)

[Listener](https://en.wikipedia.org/wiki/Event_(computing)#Event_handler)

[Event-driven programming Wikipedia](https://en.wikipedia.org/wiki/Event-driven_programming)

[Event Loop](https://en.wikipedia.org/wiki/Event_loop)

[Message queue](https://en.wikipedia.org/wiki/Message_queue)

[Event Queue](https://gameprogrammingpatterns.com/event-queue.html)

[Call Stack](https://en.wikipedia.org/wiki/Call_stack)

[Publish–subscribe pattern](https://en.wikipedia.org/wiki/Publish%E2%80%93subscribe_pattern)

[What Is a Database?](https://www.oracle.com/database/what-is-database/)

[Full Duplex (FDX)](https://en.wikipedia.org/wiki/Duplex_(telecommunications)#FULL-DUPLEX)

[What is a packet?](https://kb.iu.edu/d/anyq)

[Connectionless Protocol](https://www.sciencedirect.com/topics/computer-science/connectionless-protocol)
