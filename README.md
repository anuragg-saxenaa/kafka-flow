# Kafka Flow Visualization

A real-time Kafka message flow visualization application that helps developers understand how messages flow through a Kafka system.

## Features

- **Real-time Message Visualization**: See messages as they flow through the Kafka system in real-time
- **Message Flow Details**: View detailed information about each message including:
  - Message content
  - Status (SENT/RECEIVED)
  - Timestamp
  - Partition number
  - Offset
  - Consumer ID
- **Kafka Configuration Display**: View current Kafka configuration including:
  - Topic name
  - Number of partitions
  - Replication factor
  - Consumer group information
- **Interactive UI**: Send messages and see them flow through the system
- **Docker Support**: Easy deployment with Docker Compose

## Architecture

The application consists of:
- **Frontend**: React application with WebSocket connection to backend
- **Backend**: Spring Boot application that:
  - Connects to Kafka as both producer and consumer
  - Stores message history in MongoDB
  - Provides WebSocket endpoints for real-time updates
- **Kafka**: Message broker for handling message flow
- **MongoDB**: Database for storing message history
- **Zookeeper**: Required for Kafka operation

## Setup and Running

### Prerequisites
- Docker and Docker Compose
- Java 21
- Node.js 18+

### Running with Docker Compose
1. Clone the repository
2. Navigate to the project root
3. Run `docker-compose up`
4. Access the application at http://localhost:3000

### Running Locally
1. Start Kafka and Zookeeper
2. Start MongoDB
3. Run the backend: `cd backend && ./mvnw spring-boot:run`
4. Run the frontend: `cd frontend && npm start`

## Recent Updates

- Added Docker Compose support for easy deployment
- Enhanced message flow visualization with consumer details
- Improved error handling and connection management
- Added support for multiple consumers and partitions
- Implemented message history persistence in MongoDB

## Future Features

1. **Enhanced Visualization**
   - Add visual representation of message flow between partitions
   - Implement message tracing across multiple consumer groups
   - Add timeline view of message flow

2. **Advanced Analytics**
   - Message throughput metrics
   - Latency measurements
   - Consumer lag visualization
   - Partition distribution analysis

3. **User Experience Improvements**
   - Custom topic creation and management
   - Consumer group management interface
   - Message filtering and search capabilities
   - Dark/light theme support

4. **Monitoring and Alerts**
   - Set up alerts for consumer lag
   - Monitor broker health
   - Track message processing delays
   - Configure notification thresholds

5. **Security Enhancements**
   - Add authentication and authorization
   - Implement SSL/TLS for Kafka connections
   - Role-based access control
   - Audit logging

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details. 