# **Number Classification API**  

## **Overview**  
This API classifies a given number based on its mathematical properties and provides a fun fact about it.  

## **Features**  
- Determines if the number is **prime**  
- Checks if the number is **perfect**  
- Identifies **Armstrong numbers**  
- Classifies the number as **even** or **odd**  
- Computes the **sum of its digits**  
- Retrieves a **fun fact** from the Numbers API  

## **Technologies Used**  
- **FastAPI** for building the API  
- **Uvicorn** as the ASGI server  
- **Requests** library for external API calls  


## **Usage**  
1. Run the API locally:  
   ```sh
   uvicorn main:app --reload
   ```
2. Access the API at:  
   ```
   http://127.0.0.1:8000/api/classify-number?number=371
   ```



#### **Success Response (200 OK)**  
```json
{
    "number": 371,
    "is_prime": false,
    "is_perfect": false,
    "properties": ["armstrong", "odd"],
    "digit_sum": 11,
    "fun_fact": "371 is an Armstrong number because 3^3 + 7^3 + 1^3 = 371"
}
```

#### **Error Response (400 Bad Request)**  
```json
{
    "number": "invalid_input",
    "error": true
}
```

## **Testing the API**  
### **Using Browser**  
Visit:  
```
http://127.0.0.1:8000/api/classify-number?number=371
```

### **Using Swagger UI**  
Access the interactive documentation at:  
```
http://127.0.0.1:8000/docs
```





## **Deployment**  
To deploy the API, use platforms like:  
- **Railway**  
- **Render**  
- **Vercel**  
- **Heroku**  

