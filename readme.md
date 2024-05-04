kafka message broking minor project by Ashim

open terminal:
cd .\kafka\
docker-compose up -d

Docker window opens
Then, kafka>>kafdrop>> Open in Broswer. Then, Kafdrop Broker list indow appears


then in new terminal cd .\app\
python -m venv .\venv\ for creating virtual working env and activate it using .\venv\Scripts\activate 
then, pip install fastapi uvicorn


then, in terminal:
uvicorn main:app --reload



int thunderclient send 
1. GET request at http://:localhost:8000/-->"Welcome home" aaucha


in terminal again:
1. pip install aiokafka


again in terminal:
cd .\app\
uvicorn main:app --reload



Now for testing:
1. Go to thunderclient:
2. in Json content: {
    "message";"HEllo mesg consumer 1"
}in Body
3. Post request at  http://:localhost:8000/create_message and SEND
4. Response comes NULL maybe
5. Go check at Kafdrop:Broker-List
5.1. Reload the page
5.2. click on View Message and again on viewmessages click and now u can see :  {
    "message";"HEllo mesg consumer 1"
}
ALso check in Terminal u can see Consumer msg: ConsumerRecord(topic=''...)


6. again in body part change JSON to :{
    "message";"HEllo mesg consumer 2"
}
and check terminal as well as view message box in KAFDROP window in browser, likewise in step 2 to step 5.2







