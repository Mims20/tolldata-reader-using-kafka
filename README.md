# Top Traffic Simulator and Streaming Data Consumer

This project consists of two scripts: one for simulating top traffic data and another for consuming streaming data and storing it in a MySQL database.

## Top Traffic Simulator

The `top_traffic_simulator.py` script simulates top traffic data by generating random vehicle information and sending it to a Kafka topic named 'toll'. Each message includes vehicle ID, vehicle type, plaza ID, and timestamp.

### Usage

1. Ensure that Kafka is running on `localhost:9092`.
2. Run the `top_traffic_simulator.py` script.
3. The script generates and sends simulated traffic data to the 'toll' Kafka topic.

## Streaming Data Consumer

The `streaming_data_consumer.py` script consumes streaming data from the 'toll' Kafka topic, processes it, and inserts it into a MySQL database table named 'livetolldata'.

### Prerequisites

- MySQL database should be running on `localhost`.
- The database schema should have a table named 'livetolldata'.
- Kafka should be running on `localhost:9092`.

### Usage

1. Ensure that MySQL database and Kafka are running.
2. Run the `streaming_data_consumer.py` script.
3. The script consumes messages from the 'toll' Kafka topic, transforms the data, and inserts it into the 'livetolldata' table in the MySQL database.

## Database Configuration

Ensure that the database credentials (host, database name, username, and password) are correctly configured in the script.

## Dependencies

- Kafka Python client library (`kafka-python`)
- MySQL Connector Python library (`mysql-connector-python`)

Install the dependencies using `pip install -r requirements.txt`.

## Notes

- Adjust the simulation parameters and database configuration according to your requirements.
- Ensure that Kafka and MySQL are properly configured and running before executing the scripts.
