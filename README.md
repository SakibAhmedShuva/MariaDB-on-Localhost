# MariaDB Docker Integration with Python

This project demonstrates how to set up MariaDB using Docker and interact with it using Python. It includes basic database operations using mysql-connector-python and pandas.

## Prerequisites

- Docker
- Python 3.x
- Required Python packages:
  - mysql-connector-python
  - pandas

## Installation

1. Install required Python packages:
```bash
pip install mysql-connector-python pandas
```

2. Pull and run MariaDB Docker container:
```bash
docker run --name my-mariadb -e MYSQL_ROOT_PASSWORD=1234 -p 3306:3306 -d mariadb:10.5
```

## Project Structure

```
mariadb-docker-python/
│   README.md
│   mariadb.ipynb
│   requirements.txt
```

## Configuration

The database connection is configured with the following parameters:
- Host: localhost
- Port: 3306
- User: root
- Password: 1234
- Database: sample_db (created by the script)

## Features

1. Database Operations:
   - Create database and table
   - Insert sample data
   - Query data using pandas
   - Update records
   - Display results

2. Sample Table Structure (employees):
   - id (INT, AUTO_INCREMENT, PRIMARY KEY)
   - name (VARCHAR(100))
   - age (INT)
   - salary (DECIMAL(10,2))

## Usage

1. Start the MariaDB container:
```bash
docker start my-mariadb
```

2. Run the Python script:
```bash
python main.py
```

## Docker Commands

- Start container: `docker start my-mariadb`
- Stop container: `docker stop my-mariadb`
- Remove container: `docker rm my-mariadb`
- Check container logs: `docker logs my-mariadb`

## Error Handling

The code includes error handling for:
- Database connection failures
- Query execution errors
- Data reading errors

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.
