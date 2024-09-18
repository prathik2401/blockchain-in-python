# Simple Blockchain in Python

This project implements a simple blockchain and a basic API using Flask. The blockchain supports basic functionalities such as mining new blocks, adding transactions, and resolving conflicts between nodes.

## Installation

1. **Clone the repository**:
    ```sh
    git clone https://github.com/prathik2401/blockchain-in-python.git
    cd blockchain-in-python
    ```

2. **Create a virtual environment**:
    ```sh
    python -m venv venv
    ```

3. **Activate the virtual environment**:
    - On Windows:
        ```sh
        venv\Scripts\activate
        ```
    - On macOS/Linux:
        ```sh
        source venv/bin/activate
        ```

4. **Install the dependencies**:
    ```sh
    pip install -r requirements.txt
    ```

## Running the Application

1. **Start the Flask server**:
    ```sh
    python blockchain.py
    ```

2. **Access the API**:
    Open your web browser and go to `http://127.0.0.1:5000`.

## API Endpoints

- **Mine a new block**:
    - **URL**: `/mine`
    - **Method**: `GET`
    - **Description**: Mines a new block and adds it to the blockchain.

- **Create a new transaction**:
    - **URL**: `/transactions/new`
    - **Method**: `POST`
    - **Description**: Adds a new transaction to the list of transactions.
    - **Payload**:
        ```json
        {
            "sender": "address_of_sender",
            "recipient": "address_of_recipient",
            "amount": 10
        }
        ```

- **Get the full blockchain**:
    - **URL**: `/chain`
    - **Method**: `GET`
    - **Description**: Returns the full blockchain.

- **Register new nodes**:
    - **URL**: `/nodes/register`
    - **Method**: `POST`
    - **Description**: Registers new nodes in the network.
    - **Payload**:
        ```json
        {
            "nodes": ["http://127.0.0.1:5001"]
        }
        ```

- **Resolve conflicts**:
    - **URL**: `/nodes/resolve`
    - **Method**: `GET`
    - **Description**: Resolves conflicts between nodes by replacing the chain with the longest one in the network.

## Testing

To test the application, you can use tools like `curl` or Postman to interact with the API endpoints.

## License

This project is licensed under the MIT License.  See the LICENSE file for details.
