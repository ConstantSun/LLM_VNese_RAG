# LLM_VNese_RAG
RAG, langchain, claude,sbert

# How to run:
- Open all .py file and find all # TODO , follow TODO description to change the values.
- Suppose you're running on EC2, make sure EC2 role has following permissions:

Permission: AdminAccess

Trust Relationship:
```
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Principal": {
                "Service": "ec2.amazonaws.com"
            },
            "Action": "sts:AssumeRole"
        },
        {
            "Effect": "Allow",
            "Principal": {
                "AWS": "arn:aws:sts::<your acc ID>:assumed-role/<your EC2 instance Role>/<your EC2 instance ID>"
            },
            "Action": "sts:AssumeRole"
        }
    ]
}
```
- Make sure your Opensearch Collection has the right Data access policies for your EC2 role access:
![image](https://github.com/ConstantSun/LLM_VNese_RAG/assets/26327367/67eabf7b-e910-4688-a3d3-741764f9d675)

- Prepare env with python ^3.10.12 and pip ^23.3.1
- Run as following:
  ```
  $ pip install -r requirements.txt
  $ streamlit run webapp.py 
  ```
Then you'll see a website, looking like this: 
<img width="1393" alt="image" src="https://github.com/ConstantSun/LLM_VNese_RAG/assets/26327367/30140910-9d42-4198-b176-19535e79ae6d">

  
