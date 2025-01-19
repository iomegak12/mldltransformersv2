# Dockerizing the server

This should result in a directory structure that looks like this:
```
..
└── no-batch
    ├── app/
    │   ├── main.py (server code)
    │   └── lgbm_model.pkl
    ├── requirements.txt (Python dependencies)
    ├── examples.json (prediction to test the server)
    ├── README.md (this file)
    └── Dockerfile
```


## Make request to the server

curl -X POST http://localhost:80/predict -d @./examples.json -H "Content-Type: application/json"
