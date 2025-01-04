# SQL-Injection-Detection
SQL Injection Detection Using Machine Learning

# API in python

    import requests
  
    url = "http://127.0.0.1:5000/api/check_query"
    query = { "query": "SELECT * FROM users WHERE id = 1 OR 1=1"}
    response = requests.post( url , json=query )

    response = response.json()

    print(f"\nResponse : { response }\n")

    print("Model Prediction for the Query         : " , response["Model Prediction for the Query"]          )
    print("Prediction Probability of Class [ 0 ]  : " , response["Prediction Probability of Class [ 0 ]"]   ) 
    print("Prediction Probability of Class [ 1 ]  : " , response["Prediction Probability of Class [ 1 ]"]   )
    print("SQL Injection Result                   : " , response["SQL Injection Result"]                    )
    print("RESULT                                 : " , response["RESULT"]                                  )

# API in curl

    Curl : curl -X POST http://127.0.0.1:5000/api/check_query -H "Content-Type: application/json" -d '{"query": "SELECT * FROM users WHERE id = 1"}'
