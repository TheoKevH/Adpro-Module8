# Module 8 ADPRO

**Name**: Theodore Kevin Himawan

**NPM**: 2306210973

**Class**: Adpro A

![Picture of Jeff](https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcSdN5rX5QLfUec1pYyrLUDgcjMIK_eUI17oSKqGFnE7LfUS4e052YE128lzxCuxSvk6F5UAsd0jl7NKHSoyncNrUw)

## Reflection Module 8
> 1. What are the key differences between unary, server streaming, and bi-directional streaming RPC (Remote Procedure Call) methods, and in what scenarios would each be most suitable?

<p align="justify">Unary RPC is a one-to-one request-response where the client sends a single request and gets a single response. It is suitable for simple queries like fetching user info. Server streaming allows the client to send one request and receive a stream of responses. It is suitable for things like receiving live data updates. Bi-directional streaming RPC lets both client and server send messages in a stream independently and simultaneously, making it best for real-time chat apps or collaborative tools where constant two-way communication is needed.</p>

> 2. What are the potential security considerations involved in implementing a gRPC service in Rust, particularly regarding authentication, authorization, and data encryption?

<p align="justify">When building a gRPC service in Rust, security considerations include implementing authentication (for example JWT) to verify client identity and enforcing authorization rules to control access to specific resources or methods.</p>

> 3. What are the potential challenges or issues that may arise when handling bidirectional streaming in Rust gRPC, especially in scenarios like chat applications?

<p align="justify">In bidirectional streaming with Rust gRPC, challenges include managing multiple messages at once, keeping the connection open without blocking, and handling dropped or slow clients.</p>

> 4. What are the advantages and disadvantages of using the `tokio_stream::wrappers::ReceiverStream` for streaming responses in Rust gRPC services?

<p align="justify">For the advantage, ReceiverStream is easy to use for sending async messages in Rust gRPC, making it good for simple streaming. For the disadvantage, it can be less efficient for high-load apps and harder to manage if you need fine control over backpressure or cancellation.</p>

> 5. In what ways could the Rust gRPC code be structured to facilitate code reuse and modularity, promoting maintainability and extensibility over time?

<p align="justify">To promote reuse and modularity in Rust gRPC, structure your code by separating concerns, such as placing proto-generated code in its own module, define services and handlers in separate files, and use traits for shared logic. Group similar logic into reusable utility modules, and implement middleware-like layers for cross-cutting concerns. This keeps the code clean, testable, and easier to extend as your app grows.</p>

> 6. In the MyPaymentService implementation, what additional steps might be necessary to handle more complex payment processing logic?

<p align="justify">Some additional steps are implementation with external payment gateways, logging, error handling, and database updates to handle complex payment logic.</p>

> 7. What impact does the adoption of gRPC as a communication protocol have on the overall architecture and design of distributed systems, particularly in terms of interoperability with other technologies and platforms?

<p align="justify">Adopting gRPC improves performance and type safety in distributed systems but may reduce interoperability with non-gRPC systems due to its use of Protocol Buffers and HTTP/2, requiring extra tools or gateways for integration with older tech stacks.</p>

> 8. What are the advantages and disadvantages of using HTTP/2, the underlying protocol for gRPC, compared to HTTP/1.1 or HTTP/1.1 with WebSocket for REST APIs?

<p align="justify">HTTP/2 offers advantages like multiplexing (multiple requests over one connection), header compression, and lower latency, making it faster and more efficient than HTTP/1.1. It is more structured and integrates cleanly with gRPC for bidirectional streaming. However, it’s more complex to debug, not all proxies handle it well, and browser support for gRPC over HTTP/2 is limited, especially compared to REST with WebSocket.</p>

> 9. How does the request-response model of REST APIs contrast with the bidirectional streaming capabilities of gRPC in terms of real-time communication and responsiveness?

<p align="justify">REST uses a simple request-response model, sending one request and waiting for one reply, which limits real-time interaction. gRPC with bidirectional streaming allows both client and server to send messages anytime, enabling faster, real-time communication like in chats or live updates.</p>

> 10. What are the implications of the schema-based approach of gRPC, using Protocol Buffers, compared to the more flexible, schema-less nature of JSON in REST API payloads?

<p align="justify">gRPC's schema-based approach with Protocol Buffers ensures strict data structure, faster serialization, and better type safety, but it's less flexible and harder to inspect than JSON in REST, which is more readable and easier to improve.</p>