# EctoProbe

EctoProbe is a Node.js and React.js-based application designed for monitoring and analyzing environmental data collected from exotic physics detection devices. Whether you're using EMF detectors, manatometers, ground-penetrating radar, or GPS loggers, EctoProbe serves as the central hub for processing, visualizing, and analyzing your data.

---

## Features

- **Multi-Device Support**: Seamlessly integrates with various detection devices, including:
  - **EMF detectors**
  - **Manatometers**
  - **Ground-penetrating radar**
  - **GPS loggers**
- **Web-Based Interface**:
  - Built with the latest stable versions of React.js and Node.js.
  - Intuitive, responsive design for use on desktops, tablets, and embedded systems.
- **Advanced Data Storage and Analysis**:
  - Long-term storage with support for:
    - **SQLite**
    - **PostgreSQL**
    - **MySQL**
    - **Microsoft SQL Server**
  - Caching with Redis for high-performance data access.
  - Integration with S3, Data Lake, and Glue notebooks for AI and machine learning pipelines.
- **Expanded Log Management**:
  - Integration with OpenSearch, Elasticsearch, Loki, and Prometheus for robust log storage.
  - Supports OpenSearch Dashboards, Grafana, and Graylog GUIs for enhanced visibility.
- **Standalone or Integrated Use**:
  - Operates independently or alongside **SkinwalkerOS** and **SkinwalkerPi**.
  - Ideal for embedded devices, development, and testing environments.
- **Real-Time Monitoring**:
  - Live data streams with customizable dashboards.
  - Data alerts and anomaly detection.

---

## Importance for Data Science and Research

EctoProbe is specifically designed to cater to data science initiatives focusing on exotic physics, UAP (Unidentified Aerial Phenomena), and paranormal phenomena. Its features enable:

- **Comprehensive Data Collection**: Capture and store large datasets from diverse sources for analysis.
- **Advanced Analytics**: Utilize tools like Grafana and Glue notebooks for detailed examination of trends and anomalies.
- **Machine Learning Integration**: Feed data into AI pipelines for predictive modeling and pattern recognition.
- **Collaboration and Accessibility**: Use web-based tools to share findings and work collaboratively in multidisciplinary teams.

By providing a modular, extensible, and user-friendly platform, EctoProbe empowers researchers to uncover insights into phenomena that challenge conventional understanding.

---

## Prerequisites

- Node.js 18 or later.
- A compatible detection device (EMF detector, manatometer, etc.).
- An RDBMS system (SQLite, PostgreSQL, MySQL, or others).
- Redis for caching (optional but recommended).
- S3 or compatible storage for advanced AI integrations (optional).
- Access to a terminal or SSH client.

---

## Installation

1. Clone the EctoProbe repository:

   ```bash
   git clone git@github.com:BeyondTheHorizonLabs/EctoProbe.git
   cd EctoProbe
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Configure the application by editing the `config.json` file:

   ```json
   {
     "database": {
       "type": "postgres",
       "host": "localhost",
       "port": 5432,
       "username": "username",
       "password": "password",
       "database": "ectoprobe"
     },
     "redis": {
       "host": "localhost",
       "port": 6379
     },
     "aws": {
       "s3_bucket": "your-s3-bucket",
       "region": "us-west-2"
     },
     "port": 3000,
     "devices": {
       "emf": true,
       "gps": true,
       "radar": true
     }
   }
   ```

4. Start the application:

   ```bash
   npm start
   ```

   The application will run on [http://localhost:3000](http://localhost:3000).

---

## Usage

### Adding Devices

1. Ensure the device is properly connected.
2. Update the `config.json` file to include the new device.
3. Restart the application to detect the changes.

### Viewing Data

1. Open [http://localhost:3000](http://localhost:3000) in your browser.
2. Use the dashboard to monitor real-time data streams, visualize trends, and perform detailed analyses.

### Advanced Integrations

- **Log Storage and Visualization**:
  - Use OpenSearch Dashboards or Grafana to gain actionable insights from collected logs.
  - Integrate with Graylog for enhanced logging capabilities.
- **Machine Learning Pipelines**:
  - Store data in S3 and analyze it using Data Lake and Glue notebooks.
  - Apply AI models to identify correlations and predict outcomes.

---

## License

This project is licensed under the [MIT License](LICENSE).
