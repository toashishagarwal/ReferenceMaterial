# Introduction
ChromaDB is an open source vector DB that is needed for storing & searching the documents or texts

There are multiple methods to install & get started with ChromaDB

## Method 1: Python Installation (Recommended)
Prerequisites:

- Python 3.7 or higher
- pip (comes with Python)

Steps:

### Check Python installation
```bash
python --version
pip --version
```

### Create a virtual environment (recommended)
```bash
python -m venv chroma-env
chroma-env\Scripts\activate
```

### Install ChromaDB
```bash
pip install chromadb
```

### Verify installation
```bash
python -c "import chromadb; print('ChromaDB installed successfully')"
```

### Basic usage test
```bash
import chromadb

# Create a client
client = chromadb.Client()

# Create a collection
collection = client.create_collection("test_collection")

print("ChromaDB is working!")
```

## Method 2 ChromaDB Server Installation
For running ChromaDB as a standalone server:

### Install ChromaDB with server dependencies
```bash
pip install chromadb[server]
```

### Start the ChromaDB server
```bash
chroma run --host localhost --port 8000
```

### Verify server is running

Open browser and go to 
```bash
http://localhost:8000/api/v2/heartbeat
```
Should return {"nanosecond heartbeat": timestamp}


### Connect to server from Python
```bash
import chromadb

client = chromadb.HttpClient(host='localhost', port=8000)
print("Connected to ChromaDB server")
```

## Method 3: Docker Installation
Prerequisites:
- Docker Desktop for Windows

Steps:

### Pull ChromaDB Docker image
```bash
docker pull chromadb/chroma
```

### Run ChromaDB container
```bash
docker run -p 8000:8000 chromadb/chroma
```

### Run with persistent storage
```bash
docker run -p 8000:8000 -v chroma-data:/chroma/chroma -e IS_PERSISTENT=TRUE chromadb/chroma
```

### Test connection
```bash
import chromadb

client = chromadb.HttpClient(host='localhost', port=8000)
client.heartbeat()  # Should return heartbeat
```

----- 
After installation, you need to create a collection first. Think of it as a table in RDBMS language. 
Then you also need a persistent directory name to persist the collection.

