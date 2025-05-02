# Module 8 ADPRO

Name: Theodore Kevin Himawan
NPM: 2306210973
Class: Adpro A

## Reflection
> 1. What are the key differences between unary, server streaming, and bi-directional streaming RPC (Remote Procedure Call) methods, and in what scenarios would each be most suitable?

<p align="justify">Unary RPC is a one-to-one request-response where the client sends a single request and gets a single response. It is suitable for simple queries like fetching user info. Server streaming allows the client to send one request and receive a stream of responses. It is suitable for things like receiving live data updates. Bi-directional streaming RPC lets both client and server send messages in a stream independently and simultaneously, making it best for real-time chat apps or collaborative tools where constant two-way communication is needed.</p>

> 2. What are the potential security considerations involved in implementing a gRPC service in Rust, particularly regarding authentication, authorization, and data encryption?

<p align="justify">When building a gRPC service in Rust, security considerations include implementing authentication (for example JWT) to verify client identity and enforcing authorization rules to control access to specific resources or methods.</p>

> 3. What are the potential challenges or issues that may arise when handling bidirectional streaming in Rust gRPC, especially in scenarios like chat applications?

<p align="justify"></p>
